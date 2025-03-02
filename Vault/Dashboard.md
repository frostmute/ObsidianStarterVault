---
banner: "![[banner-dashboard.jpg]]"
include_in_navbar: true
navbar_name: Dashboard
tags:
  - dashboard
cssclasses:
  - cards
  - dashboard
---

# Dashboard

>[!multi-column]
>>[!blank-container]
>>## 🏠  Navigation
>>[[00 Concept Board/Concept Board|💡  Concept Board →]]
>>[[01 Journal/Journal|📘 Journal →]]
>>[[02 Learning/Learning|🎓  Learning →]]
>>[[03 Notes/Notes|🗒️  Notes →]]
>>[[04 Projects/Projects|📐  Projects →]]
>>[[05 Resources/Resources|ℹ️  Resources →]]
>>[[06 Spaces/Spaces|📦  Spaces →]]
>
>>[!blank-container]
>>## 📐  Projects (`$=dv.pages('"Projects" and #project').length`)
>>```dataviewjs
>>let projectList = [];
>>let projects = dv.pages('"Projects" and #dashboard and !#projects');
>>projects = projects.filter(obj => obj.is_active === true);
>>for(let i=0; i<projects.length; i++){
>>	projectList.push(`[[${projects[i].file.path}|${projects[i].file.path.split('/')[projects[i].file.path.split('/').length-2]} →]]`)
>>}
>>dv.list(projectList)
>>```
---
>[!multi-column]
>>[!blank-container]
>>## 🚀 Upcoming Launches
>>```dataviewjs
>>function construct_elements(data) {
>>for(let i=0; i<data.length; i++){
>>	let missions = [];
>>	for(let j=0; j<data[i].missions.length; j++){missions.push(data[i].missions[j].name)}
>>	dv.el("div", 
>>	`<div class="tailwind"><div class='block py-2'><div class="text-xl font-bold text-gray-800">${data[i].name}<small class="float-right text-gray-600 font-semibold text-sm pl-2">${data[i].date_str}</small></div> <div class="text-sm font-semibold text-gray-600">Vehicle: ${data[i].vehicle.name}</div> <div class="text-sm font-semibold text-gray-600">Missions: ${missions}</div> <div class="text-sm text-gray-600"> ${data[i].launch_description} </div> </div> </div>
>>	`
>>	)
>>}
>>}
>>let response = await fetch('https://fdo.rocketlaunch.live/json/launches/next/5') 
>>response.json().then(j => construct_elements(j.result))
>>```
>
>>[!blank-container]
>>## &emsp;🛰️Space Image of the Day
>>```dataviewjs
>>const {NASAImageOfTheDay} = customJS;
>>let element = this.container.createEl('div', {cls: ["tailwind"]});
>>let apiKey = "PSrdswa5IKTJeSc007kTh8Vg6Y4A8mrxyIIHTeGp";
>>await NASAImageOfTheDay.getImage(element, apiKey);
>>```

### Recently Changed
```dataviewjs
function converteTime(time){
	// Convert from ms to minutes
	let convertedTime = ""
	time = time/60000; // time in minutes

	if(time < 60){
		convertedTime = `${Math.ceil(time)} minutes ago`;
	} else if (time < 1440){
		convertedTime = `${Math.ceil(time/60)} hours ago`
	} else {
		convertedTime = `${Math.ceil(time/1440)} days ago`
	}	
	return convertedTime
}

for (let group of dv.pages('!"_data_"').sort(k => k.file.mtime, 'desc').limit(10).groupBy(p => p.page)) {
	dv.table(["Name", "Date Modified", ""], 
		group.rows
			.sort(k => k.file.mtime, 'desc')
			.map(k => [
			k.file.link, 
			converteTime(Date.now()-k.file.mtime),
			`<small>[[${k.file.path}|View →]]</small>`
			]))}
```

### **Stats**
Number of files: `$=dv.pages('!"_data_"').length`
Number of notes: `$=dv.pages('"Notes" and !#dashboard').length`
Number of concepts: `$=dv.pages('"Concept Board" and !#dashboard').length`

---
### 📰 Recent News
>
> ```dataviewjs
> const {News} = customJS;
> let element = this.container.createEl('div', {cls: ["tailwind"]});
> let newsCategory = 'stocks';
> let articleCount = '6';
> let apiKey = 'e40a3e9b49a4248f96e15459daa4a434';
> await News.listNews(element, newsCategory, articleCount, apiKey);
>

 ---
 
 ```dataviewjs
 const {Navbar} = customJS;
 await Navbar.createNavbar(app, dv); 
 ```
 