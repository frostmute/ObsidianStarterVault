---
searchTerm: book
searchType: "tags"
searchText: 
cusfield: 
searchDate: 2022-08-03
excludeTag: 
exFolder: BT_Example/88-Template,BT_Example/88-Template/tp
limit: 
cssclasses: cards
---

> [!info] 提示
> - 为安全起见，删除文件，并没有真正删除，只是把文件移动到了Ob库文件夹.trash 目录

```dataviewjs
// [obsidian-snippets/dataviewjs.acrossVaultWordCount-v0.0.11.md at main · torantine/obsidian-snippets (github.com)](https://github.com/torantine/obsidian-snippets/blob/main/dataviewjs.acrossVaultWordCount-v0.0.11.md)
// modified by Blue-topaz-example Cuman
dv.paragraph("### 通过下拉框筛选检索条件<br><br>");
const metaeditEnabled = app.plugins.enabledPlugins.has("metaedit");
if (metaeditEnabled === true) {
    const { update } = this.app.plugins.plugins["metaedit"].api;
    const {createButton} = app.plugins.plugins["buttons"]
    const thisFile = dv
        .pages()
        .where((f) => f.file.path == dv.current().file.path);
    let searchType = dv.current().searchType;
    let searchTerm = dv.current().searchTerm ?? "";
    let limit = dv.current().limit ?? "";
    let searchText = dv.current().searchText ?? "";
    let searchDate = dv.current().searchDate;
    let cusfield =dv.current().cusfield??"";
    let cusfield_arr=cusfield?.split(',')
    let exFolder = dv.current().exFolder??'';	
	let excludeTag =  dv.current().excludeTag??'';
    function formatDate(date) {
        var d = new Date(date),
            month = "" + (d.getMonth() + 1),
            day = "" + d.getDate(),
            year = d.getFullYear();
        if (month.length < 2) month = "0" + month;
        if (day.length < 2) day = "0" + day;
        return [year, month, day].join("-");
    }
    searchDate = formatDate(searchDate);
    let mtime = dv.pages().where((p) => formatDate(p.file.mtime) == searchDate);
    const dateMaker = (pn, fpath) => {
        const file = this.app.vault.getAbstractFileByPath(fpath);
        const textBox = this.container.createEl("input");
        textBox.type = "date";
        textBox.value = searchDate;
        textBox.placeholder = "Enter tag to search for";
        console.log(textBox.value);
        textBox.addEventListener("input", async (evt) => {
            evt.preventDefault();
            await update(pn, '"' + textBox.value + '"', file);
        });
        return textBox;
    };
    const searchTypeDropdownMaker = (pn, fpath) => {
        const file = this.app.vault.getAbstractFileByPath(fpath);
        const optionsText = ["按标签", "按修改日期"];
        const optionsValue = ["tags", "mdate"];
        const dropdown = this.container.createEl("select");
        const option1 = dropdown.createEl("option");
        option1.text = optionsText[0];
        option1.value = optionsValue[0];
        const option2 = dropdown.createEl("option");
        option2.text = optionsText[1];
        option2.value = optionsValue[1];
        dropdown.selectedIndex != null
            ? (dropdown.selectedIndex = optionsValue.indexOf(searchType.toString()))
            : (dropdown.selectedIndex = 0);
        dropdown.addEventListener("change", async (evt) => {
            evt.preventDefault();
            await update(pn, optionsValue[dropdown.selectedIndex], file);
        });
        return dropdown;
    };
    const inputMaker = (pn, input_value, fpath) => {
        const file = this.app.vault.getAbstractFileByPath(fpath);
        const input = this.container.createEl("input");
        input.setAttribute("name", "input");
        input.setAttribute("id", pn);
        input.setAttribute("placeholder", "输入值后回车生效");
        input.setAttribute("value", input_value);
        input.addEventListener("keyup", async function (event) {
            event.preventDefault();
            if (event.keyCode === 13) {
                await update(pn, this.value, file);
            }
        });
        return input;
    };
    const tagsDropdownMaker = (pn, fpath) => {
        const file = this.app.vault.getAbstractFileByPath(fpath);
        const tags = Object.keys(app.metadataCache.getTags()).sort();
        tags.unshift("#");
        const dropdown = this.container.createEl("select");
        dropdown.setAttribute("multip", "");
        dropdown.setAttribute("id", "filter_tags");
        tags.forEach((tag, index) => {
            var opt = tag;
            var el = dropdown.createEl("option");
            opt != "#" ? (el.textContent = opt) : (el.textContent = "All Pages");
            let searchTerm_arr = searchTerm.split(",");
            searchTerm_arr.forEach((value) => {
                opt === "#" + value ? el.setAttribute("choose", "") : "";
            });
			el.value = opt;
          
            dropdown.appendChild(el);
        });

        tags.indexOf("#" + searchTerm.toString()) < 0
            ? (dropdown.selectedIndex = 0)
            : (dropdown.selectedIndex = tags.indexOf("#" + searchTerm.toString()));
        dropdown.addEventListener("change", async (evt) => {
            evt.preventDefault();
            let obj = document.getElementById("filter_tags");
            const tag_select = obj.querySelector("[hidden]")?.value;
            let tag_select_arr = tag_select.split(",");
            let tag_select_arr_res = [];
            tag_select_arr.forEach((value) => {
                if (value != "#") {
                    value = value.replace("#", "");
                    tag_select_arr_res.push(value);
                } else {
                    tag_select_arr_res = [];
                }
            });
            //await update(pn,tag_select, file)
            await update(pn, tag_select_arr_res.join(), file);
        });
        return dropdown;
    };
      
const keysDropdownMaker = (pn,pv, fpath,source) => {
		const file = this.app.vault.getAbstractFileByPath(fpath)
		let allkeys = []
		let filefield=['file.name','file.link','file.folder','file.outlinks','file.inlinks']
		let sourceTag_arr=source?.split(',')
		let valueOfsourceTag = join_tag(sourceTag_arr);
		if(valueOfsourceTag==='#')
		valueOfsourceTag = valueOfsourceTag.replace("#", "");
		const pages = dv.pages(valueOfsourceTag)
		pages.forEach((page, index) => {
		allkeys.push(Object.keys(page))
		})
		allkeys =unique(allkeys.flat())
		 allkeys= allkeys.concat(filefield)
		const keys = Object.values(allkeys).sort();
		keys.unshift("")
		const dropdown = this.container.createEl('select');
		 dropdown.setAttribute("multip", "");
        dropdown.setAttribute("id", "filter_field");
		keys.forEach((key, index) => {
			var opt = key
			var el = dropdown.createEl('option');
		opt != "" ? el.textContent = opt : el.textContent = "Null";
            cusfield_arr.forEach((value) => {
                opt === value ? el.setAttribute("choose", "") : "";
            });
            el.value = opt;
			dropdown.appendChild(el);
		})
		keys.indexOf(pv.toString()) < 0 ? dropdown.selectedIndex = 0 : dropdown.selectedIndex = keys.indexOf(pv.toString())
	      
		dropdown.addEventListener('change', async evt => {
			evt.preventDefault();
			let obj = document.getElementById("filter_field");
		    const field_select = obj.querySelector("[hidden]")?.value;
            let field_select_arr = field_select.split(",");
            let field_select_arr_res = [];
            field_select_arr.forEach((value) => {
                if (value != "") {
                    value = value.replace("#", "");
                    field_select_arr_res.push(value);
                } else {
                    field_select_arr_res = [];
                }
            });
            //await update(pn,tag_select, file)
            await update(pn, field_select_arr_res.join(), file);
        });
		return dropdown
	}
	///
	const exFolerDropdownMaker = (pn, fpath) => {
		const file = this.app.vault.getAbstractFileByPath(fpath)
		const folders = this.app.vault.getAllLoadedFiles().filter(i => i.children).map(folder => folder.path);
		folders.unshift("")
		const dropdown = this.container.createEl('select');
		dropdown.setAttribute("multip", ""); 
		dropdown.setAttribute("id", "exfolder"); 
		folders.forEach((folder, index) => {
			var opt = folder;
			var el = dropdown.createEl('option');
			opt != "/" ? el.textContent = opt : el.textContent = "All folder";
	let exFolder_arr=exFolder?.split(',')
	exFolder_arr?.forEach((value) => {
		opt===(value)?el.setAttribute("choose", ""):''
		})		
			el.value = opt;
			dropdown.appendChild(el);
		})
		folders.indexOf(exFolder) < 0 ? dropdown.selectedIndex = 0 : dropdown.selectedIndex = folders.indexOf(exFolder)
	dropdown.addEventListener('change', async evt => {
	evt.preventDefault();
	const dom_folder = this.container.querySelector('#exfolder');
	const exfolder_select=dom_folder.querySelectorAll("[hidden]")[0]?.value;
	let exfolder_select_arr_res=[]
	let exfolder_select_arr=	exfolder_select.split(',')
	for (var i = 0; i < exfolder_select_arr.length; i++) {
   if(exfolder_select_arr[i] ===  "")
    { exfolder_select_arr_res=[""]
    break;}
    else{
exfolder_select_arr_res.push(exfolder_select_arr[i])
    }}
	if(exfolder_select_arr_res.indexOf('/')> -1) 
	{if (exfolder_select_arr_res.length>1)
		{if(exfolder_select_arr_res.indexOf('/')=== 0) 
				exfolder_select_arr_res.shift();
			else
				exfolder_select_arr_res=['/'];}
		}
	await update(pn, exfolder_select_arr_res.join(), file)
		})
		
		
		return dropdown
	}

//////
	const extagsDropdownMaker = (pn, fpath) => {
		const file = this.app.vault.getAbstractFileByPath(fpath)
		const tags = Object.keys(app.metadataCache.getTags()).sort();
		const dropdown = this.container.createEl('select');
		dropdown.setAttribute("multip", ""); 
		dropdown.setAttribute("id", "extags"); 
		tags.unshift("")
		tags.forEach((tag, index) => {
			var opt = tag;
			var el = dropdown.createEl('option');
		opt != "#" ? el.textContent = opt : el.textContent = "All Tags";
	let excludeTag_arr=excludeTag.split(',')
	excludeTag_arr.forEach((value) => {
		opt===("#"+value)?el.setAttribute("choose", ""):''
		})
			el.value = opt;
			dropdown.appendChild(el);
		})
		tags.indexOf("#"+excludeTag) < 0 ? dropdown.selectedIndex = 0 : dropdown.selectedIndex = tags.indexOf("#"+excludeTag)
		dropdown.addEventListener('change', async evt => {
			evt.preventDefault();
		const dom_tags = this.container.querySelector('#extags');
			const excludeTag_select=dom_tags.querySelectorAll("[hidden]")[0]?.value;
let excludeTag_select_arr=	excludeTag_select.split(',')
		let excludeTag_select_arr_res=[]
		excludeTag_select_arr.forEach((value) => {
		if(value!='')
			{
			value=value.replace("#","");
			excludeTag_select_arr_res.push(value)
			}else
			{
			excludeTag_select_arr_res=[]
			}
		})	
		await update(pn, excludeTag_select_arr_res.join(), file)		
			//await update(pn, tags[dropdown.selectedIndex].slice(1), file)
		})	
		
		return dropdown;
	}	
	
    // Output
const gethtmltable = async (html) => { 
    var data = [];
    var table = html.querySelector("table");
    console.log(table,1)
      if (table) {
     var rows = table.rows;
     var row = []
     var cellContent
      for (var i = 0; i < rows.length; i++) {
        var cols = rows[i].querySelectorAll("td,th");
         cellContent = cols[0].innerHTML;
      cellContent=getDomAttr(cellContent,'a','data-href')
          row.push(cellContent);
        }
    //console.log(row)
	    row=row.filter(Boolean)
      await movetrash(row)	 
      }
  }

    dv.el("dvjs", "");
    dv.el("b", "结果限制:&ensp;", {
        attr: { "style": "font-size:1.5em;display: inline-table" },
    });
    dv.el("b", inputMaker("limit", limit, dv.current().file.path), {
       attr: { "style":"display: inline-table" },
    });
    dv.el("b", "`\`button-table2csv\``", {
        attr: { "style": "display: inline-table;" },
    });
    createButton({app, el: this.container, args: {name:'删除🗑️',class:'tiny'}, clickOverride: {click: gethtmltable, params: [document]}})
     dv.el("br")
    dv.el("b", "检索类型:&ensp;", {
        attr: { "style": "display: inline-table;font-size:1.5em;" },
    });
    dv.el("b", searchTypeDropdownMaker("searchType", dv.current().file.path), {
        attr: { "style":"display: inline-table" },
    });
    dv.el("b", "选&emsp;项:&ensp;", {
        attr: { "style": "font-size:1.5em;display: inline-table" },
    });
    if (searchType === "tags") {
        dv.el("b", tagsDropdownMaker("searchTerm", dv.current().file.path), {
            attr: { "style":"display: inline-table" },
        });
    } else if (searchType === "mdate") {
        dv.el("b", dateMaker("searchDate", dv.current().file.path), {
            attr: { "style":"display: inline-table" },
        });
    } else {
        dv.el("b","请选择有效的搜索类型", {
        attr: { "style": "font-size:1.5em;display: inline-table" },
    });
    }
     dv.el("br")
    dv.el("b", "文件过滤:&ensp;", {
        attr: { "style": "font-size:1.5em;display: inline-table" },
    });

    dv.el("b", inputMaker("searchText", searchText, dv.current().file.path), {
            attr: { "style":"display: inline-table" },
        });
    dv.el("b", "添加字段:&ensp;", {
        attr: { "style": "font-size:1.5em;display: inline-table" },
    });
    
    dv.el("b", keysDropdownMaker('cusfield',cusfield, dv.current().file.path,searchTerm), {
       attr: { "style":"display: inline-table" },
    });
    dv.el("br")
	 dv.el("b", "排除文件夹:&ensp;", {
	        attr: { "style": "font-size:1.5em;display: inline-table" },
	    });
	dv.el("b", exFolerDropdownMaker('exFolder', dv.current().file.path), {
       attr: { "style":"display: inline-table" },
    });
	 dv.el("b", "排除标签:&ensp;", {
	        attr: { "style": "font-size:1.5em;display: inline-table" },
	    });
	dv.el("b", extagsDropdownMaker('excludeTag', dv.current().file.path), {
       attr: { "style":"display: inline-table" },
    });
 
} else {
    dv.paragraph(
        "<strong>!!! 请启用 MetaEdit 插件，然后重新加载文档!!!</strong>"
    );
}

async function movetrash(paths) {
	if(paths.length>0)
	{
	let tips=paths.join("<br>");
	const result = await app.plugins.plugins['templater-obsidian'].templater.functions_generator.internal_functions.modules_array[4].static_functions.get('yesNoPrompt')("⚠️确定移除"+paths.length+"个文件？","‼️下面文件将被移动至Ob回收站(.trash):<br>"+tips);
	if(result)
	{
		paths.forEach((path) => {
      if (path)  app.vault.trash(app.vault.getAbstractFileByPath(path)) })
	}
}else
	{
	await new Notice("没有发现要移除的文件",2000);
	}
}
function getDomAttr(str,tag,attr) {
	const regexp = new RegExp(`<${tag}[^>]+${attr}=['"]([^'"]+)['"]+`, 'g') 
let m;
 let tmp
while ((m = regexp.exec(str)) !== null) {
    if (m.index === regexp.lastIndex) {
        regexp.lastIndex++;
    }

    m.forEach((match, groupIndex) => {
        tmp=match
    });
}
return tmp
    }
    
function unique(arr) {
   return Array.from(new Set(arr)) 
}
function join_tag(arr) {
		let sourceTag_arr_res=[]
		let join_tags=''
		
		if (arr.length>1)
		{ 
			arr.forEach((value) => {
				if (value) if (!value.startsWith("#")) value = "#" + value;
				sourceTag_arr_res.push(value)
				})
				join_tags=	sourceTag_arr_res.join(' or ')
				
		}else
		{
	join_tags = "#"+arr; // value of "sourceTag"
	
	 
	}

	return join_tags
}

const script = this.container.createEl("script");
script.text = `(function() {
		selectMultip = {
			register: function(id) {
				if(id)
				{
					var e = document.getElementById(id);
					render(e);
					}else
				{
					document.querySelectorAll("[multip]").forEach(function(e) {
					render(e);
				})
				}
			},
			reload: function(id, data, setData) {
				var htm = "";
				for(var i = 0; i < data.length; i++) {
					htm += '<option value="' + data[i].value + '">' + data[i].text + '</option>'
				}
				var e = document.getElementById(id);
				e.innerHTML = htm;
				render(e);
				this.setVal(id, setData);
			},
			setVal: function(id, str) {
				var type = Object.prototype.toString.call(str);
				switch(type) {
					case "[object String]":
						document.getElementById(id).val = str;
						break;
					case "[object Array]":
						document.getElementById(id).val = str.toString();
						break;
					default:
						break;
				}
			},
			getVal: function(id) {
				return document.getElementById(id).val;
			},
 
		}
 
		function render(e) {
			e.param = {
				arr: [],
				valarr: [],
				opts: []
			};
			var choosevalue = "",
				op;
			for(var i = 0; i < e.length; i++) {
				op = e.item(i);
				e.param.opts.push(op);
				if(op.hasAttribute("choose")) {
					if(choosevalue == "") {
						choosevalue = op.value
					} else {
						choosevalue += "," + op.value;
					}
 
				}
			}
			var option = document.createElement("option");
			option.hidden = true;
			e.appendChild(option);
			e.removeEventListener("input", selchange);
			e.addEventListener("input", selchange);
			
			Object.defineProperty(e, "val", {
				get: function() {
					return this.querySelector("[hidden]").value;
				},
				set: function(value) {
					e.param.valarr = [];
					var valrealarr = value == "" ? [] : value.split(",");
					e.param.arr = [];
					e.param.opts.filter(function(o) {
						o.style = "";
					});
					if(valrealarr.toString()) {
						for(var i = 0; i < valrealarr.length; i++) {
							e.param.opts.filter(function(o) {
								if(o.value == valrealarr[i]) {
									o.style = "color:var(--text-error);";
									e.param.arr.push(o.text);
									e.param.valarr.push(o.value)
								}
							});
						}
						this.options[e.length - 1].text = e.param.arr.toString();
						this.options[e.length - 1].value = e.param.valarr.toString();
						this.options[e.length - 1].selected = true;
					} else {
						this.options[0].selected = true;
					}
 
				},
				configurable: true
			})
			//添加属性choose 此属性添加到option中用来指定默认值
			e.val = choosevalue;
		}
 
		function selchange() {
			var text = this.options[this.selectedIndex].text;
			var value = this.options[this.selectedIndex].value;
			this.options[this.selectedIndex].style = "color: blue;";
			var ind = this.param.arr.indexOf(text);
			if(ind > -1) {
				this.param.arr.splice(ind, 1);
				this.param.valarr.splice(ind, 1);
				this.param.opts.filter(function(o) {
					if(o.value == value) {
						o.style = "";
					}
				});
			} else {
				this.param.arr.push(text);
				this.param.valarr.push(value);
			}
			this.options[this.length - 1].text = this.param.arr.toString();
			this.options[this.length - 1].value = this.param.valarr.toString();
			if(this.param.arr.length > 0) {
				this.options[this.length - 1].selected = true;
			} else {
				this.options[0].selected = true;
			}
		}
	})();
	selectMultip.register();
	
	`;

```

## 统计列表
```dataviewjs
dv.view("BT_Example/88-Template/script/dv_getwordcoutView", '')
```
