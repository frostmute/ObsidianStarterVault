—

—

async(e,t,n=!1,o="",s)=>{let a=new zr(this.plugin.app,e,t,o,s),A=new Promise((c,d)=>a.openAndGetValue(c,d));try{return await A}catch(c){if(n)throw c;return null}}