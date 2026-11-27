[Campus_Lost___Found.html](https://github.com/user-attachments/files/35522487/Campus_Lost___Found.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Campus Lost &amp; Found</title>
<style>
:root{--bg:#f6f7fb;--card:#fff;--tx:#1d2433;--mu:#667085;--bd:#e3e6ee;--ac:#4f46e5;--ac2:#eef0ff;--ok:#12805c;--wa:#b45309;--er:#c0262d;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px);color-scheme:light}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#12141c;--card:#1b1e29;--tx:#e8eaf2;--mu:#9aa1b5;--bd:#2c3040;--ac:#8b85ff;--ac2:#252847;--ok:#3ecf9b;--wa:#f5a524;--er:#ff6b72;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#12141c;--card:#1b1e29;--tx:#e8eaf2;--mu:#9aa1b5;--bd:#2c3040;--ac:#8b85ff;--ac2:#252847;--ok:#3ecf9b;--wa:#f5a524;--er:#ff6b72;color-scheme:dark}
*{box-sizing:border-box}html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;background:var(--bg);color:var(--tx);font:15px/1.5 system-ui,-apple-system,"Segoe UI",Roboto,sans-serif}
.wrap{max-width:980px;margin:0 auto;padding:16px}
h1{font-size:22px;margin:4px 0}p.sub{color:var(--mu);margin:0 0 12px}
nav{display:flex;gap:6px;overflow-x:auto;margin:12px 0}
nav button,.btn{border:1px solid var(--bd);background:var(--card);color:var(--tx);padding:8px 14px;border-radius:8px;cursor:pointer;font:inherit;white-space:nowrap}
nav button.on,.btn.p{background:var(--ac);color:#fff;border-color:var(--ac)}
.btn.s{padding:4px 9px;font-size:13px}.btn.d{color:var(--er)}
.card{background:var(--card);border:1px solid var(--bd);border-radius:12px;padding:16px;margin-bottom:12px}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px}
label{display:block;font-size:13px;color:var(--mu);margin-bottom:3px}
input,select,textarea{width:100%;padding:8px 10px;border:1px solid var(--bd);border-radius:8px;background:var(--bg);color:var(--tx);font:inherit}
.tw{overflow-x:auto}table{width:100%;border-collapse:collapse;font-size:14px}
th,td{text-align:left;padding:8px;border-bottom:1px solid var(--bd);vertical-align:top}th{color:var(--mu);font-weight:600}
.tag{display:inline-block;padding:2px 8px;border-radius:99px;font-size:12px;background:var(--ac2);color:var(--ac)}
.tag.rec{background:#12805c22;color:var(--ok)}.tag.strong{background:#12805c22;color:var(--ok)}.tag.mod{background:#b4530922;color:var(--wa)}.tag.weak{background:#c0262d22;color:var(--er)}
.bar{height:8px;border-radius:4px;background:var(--bd);overflow:hidden;margin:4px 0}.bar i{display:block;height:100%;background:var(--ac)}
#toast{position:fixed;left:50%;transform:translateX(-50%);bottom:calc(16px + env(safe-area-inset-bottom,0px));padding:10px 16px;border-radius:8px;color:#fff;display:none;z-index:9;max-width:90%}
.row{display:flex;gap:8px;flex-wrap:wrap;align-items:end}.row>*{flex:1;min-width:140px}
.mu{color:var(--mu)}.hide{display:none}
.mdl{position:fixed;inset:0;background:rgba(0,0,0,.55);display:none;align-items:center;justify-content:center;padding:16px;z-index:8}.mdl.show{display:flex}.mbox{width:100%;max-width:440px;margin:0}
.bk{margin-top:16px}
.th{width:48px;height:48px;object-fit:cover;border-radius:6px;float:left;margin-right:8px;cursor:zoom-in;border:1px solid var(--bd)}
.pgrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:12px}
.pgrid .card{margin:0;padding:10px}
.pgrid img{width:100%;aspect-ratio:4/3;object-fit:cover;border-radius:8px;cursor:zoom-in;display:block;margin-bottom:8px}
#pprev img{max-width:100%;max-height:220px;border-radius:8px;margin-top:10px;border:1px solid var(--bd)}
.zoom{max-width:100%;max-height:60vh;display:block;margin:0 auto;border-radius:8px}
</style>
</head>
<body>
<div class="wrap">
<h1>🎒 Campus Lost &amp; Found</h1>
<p class="sub">Register, search and smartly match lost and found belongings. Records are saved in this browser.</p>
<nav id="nav"></nav>

<section id="t-reg" class="card">
<h3 id="regTitle" style="margin-top:0">Register item</h3>
<form id="f" onsubmit="return false">
<div class="grid">
<div><label>Type</label><select id="type"><option value="Lost">Lost</option><option value="Found">Found</option></select></div>
<div><label>Item name *</label><input id="name" maxlength="60"></div>
<div><label>Category *</label><select id="cat"></select></div>
<div><label>Location *</label><input id="loc" maxlength="60" placeholder="e.g. Library, Block A"></div>
<div><label>Date *</label><input id="date" type="date"></div>
<div><label>Contact name *</label><input id="cn" maxlength="60"></div><div><label>Contact phone or email *</label><input id="ci" maxlength="60"></div>
</div>
<div style="margin-top:12px"><label>Detailed description *</label><textarea id="desc" rows="3" maxlength="300"></textarea></div>
<div class="row" style="margin-top:12px"><button class="btn p" id="saveBtn">Save item</button><button class="btn hide" id="cancelBtn">Cancel edit</button></div>
</form>
</section>

<section id="t-items" class="hide">
<div class="card"><div class="row">
<div><label>Search by ID or name</label><input id="q" placeholder="Type to search…"></div>
<div><label>Category</label><select id="fc"></select></div>
<div><label>Type</label><select id="ft"><option value="">All</option><option>Lost</option><option>Found</option></select></div>
<div><label>Status</label><select id="fs"><option value="">All</option><option>Active</option><option>Recovered</option></select></div>
</div></div>
<div class="card tw" id="list"></div>
</section>

<section id="t-pic" class="hide">
<div class="card"><h3 style="margin-top:0">Attach a picture</h3>
<div class="row"><div><label>Item *</label><select id="pi"></select></div>
<div><label>Picture *</label><input id="pf" type="file" accept="image/*"></div></div>
<div id="pprev"></div>
<div class="row" style="margin-top:12px"><button class="btn p" id="pAttach">Attach picture</button></div>
<p class="mu" style="margin-bottom:0">Pictures are resized and saved in this browser with the item. Attaching a new one replaces the old one.</p></div>
<div id="pgal" class="pgrid"></div>
</section>

<section id="t-match" class="hide">
<div class="card"><button class="btn p" id="runMatch">Run smart matching</button>
<span class="mu"> Compares active Lost items with active Found items. Recovered items are excluded.</span></div>
<div id="matches"></div>
</section>

<section id="t-hist" class="hide"><div class="card tw" id="hist"></div></section>

<section id="t-admin" class="hide">
<div class="card" id="adminBox"></div>
</section>
</div>
<div id="mdl" class="mdl"><div class="card mbox"><h3 id="mt" style="margin-top:0"></h3><div id="mb"></div><div class="row" style="margin-top:12px"><button class="btn p" id="mok"></button><button class="btn" id="mno">Cancel</button></div></div></div>
<div id="toast"></div>

<script>
var CATS=["Electronics","Books & Stationery","Bags","Clothing","ID & Cards","Keys","Accessories","Other"];
var TABS=[["reg","Register"],["items","Items"],["pic","Pictures"],["match","Smart Match"],["hist","Recovery History"],["admin","Admin"]];
var S={items:[],hist:[],cfg:{strong:80,mod:65,weak:50,pin:"1234"}},admin=false,editId=null;
var $=function(s){return document.querySelector(s)};
function esc(s){return String(s).replace(/[&<>"']/g,function(c){return {"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c]})}
function ld(k,d){try{var v=localStorage.getItem(k);return v?JSON.parse(v):d}catch(e){return d}}
function sv(){try{localStorage.setItem("clf_items",JSON.stringify(S.items));localStorage.setItem("clf_hist",JSON.stringify(S.hist));localStorage.setItem("clf_cfg",JSON.stringify(S.cfg));return true}catch(e){return false}}
function toast(m,ok){var t=$("#toast");t.textContent=m;t.style.background=ok===false?"#c0262d":"#12805c";t.style.display="block";clearTimeout(toast.h);toast.h=setTimeout(function(){t.style.display="none"},3000)}
function today(){var d=new Date();return d.getFullYear()+"-"+String(d.getMonth()+1).padStart(2,"0")+"-"+String(d.getDate()).padStart(2,"0")}
function validDate(s){if(!/^\d{4}-\d{2}-\d{2}$/.test(s))return false;var p=s.split("-").map(Number),d=new Date(p[0],p[1]-1,p[2]);
 return d.getFullYear()===p[0]&&d.getMonth()===p[1]-1&&d.getDate()===p[2]&&s<=today()&&p[0]>=2000}
function nextId(type){var pre=type==="Lost"?"L":"F",m=0;S.items.forEach(function(i){if(i.id[0]===pre)m=Math.max(m,parseInt(i.id.slice(1),10)||0)});return pre+String(m+1).padStart(3,"0")}

/* Similarity: Ratcliff/Obershelp, same idea as Python difflib.SequenceMatcher.ratio() */
function mt(a,b){if(!a.length||!b.length)return 0;var best=0,ai=0,bi=0;
 for(var i=0;i<a.length;i++)for(var j=0;j<b.length;j++){var k=0;while(i+k<a.length&&j+k<b.length&&a[i+k]===b[j+k])k++;if(k>best){best=k;ai=i;bi=j}}
 if(!best)return 0;return best+mt(a.slice(0,ai),b.slice(0,bi))+mt(a.slice(ai+best),b.slice(bi+best))}
function sim(a,b){a=a.toLowerCase().trim();b=b.toLowerCase().trim();if(!a&&!b)return 1;if(!a||!b)return 0;return 2*mt(a,b)/(a.length+b.length)}
/* Hybrid engine: stop-words, aliases, soft Jaccard (typo tolerant), coverage, sorted-token char similarity */
function cl(s){return String(s==null?'':s).replace(/\s+/g,' ').trim()}
var STOP={a:1,an:1,the:1,with:1,near:1,of:1,in:1,on:1,at:1,for:1,and:1,or:1,to:1,my:1,is:1,it:1,has:1,had:1,by:1,from:1,some:1,this:1,that:1,his:1,her:1,i:1,we:1,lost:1,found:1};
var ALI={lib:'library',libr:'library',dept:'department',canteen:'cafeteria',mess:'cafeteria',caf:'cafeteria',lab:'laboratory',aud:'auditorium',gym:'gymnasium',admin:'administration',blk:'block',bldg:'building',backpack:'bag',rucksack:'bag',flask:'bottle',earphone:'earbud',headphone:'earbud',airpod:'earbud',cellphone:'mobile',smartphone:'mobile',phone:'mobile',adapter:'charger',pendrive:'usb',spectacle:'specs',spec:'specs',eyeglasse:'specs',glasse:'specs'};
function toks(s){return cl(s).toLowerCase().replace(/[^a-z0-9 ]/g,' ').split(' ').filter(function(w){return w&&!STOP[w]}).map(function(w){if(w.length>3&&/[^s]s$/.test(w)&&!/(us|is)$/.test(w))w=w.slice(0,-1);return ALI[w]||w})}
function lev(a,b){var p=[],i,j;for(j=0;j<=b.length;j++)p[j]=j;for(i=1;i<=a.length;i++){var c=[i];for(j=1;j<=b.length;j++)c[j]=Math.min(p[j]+1,c[j-1]+1,p[j-1]+(a[i-1]===b[j-1]?0:1));p=c}return p[b.length]}
function wsim(a,b){if(a===b)return 1;var m=Math.max(a.length,b.length);if(m<4)return 0;var s=1-lev(a,b)/m;return s>=0.7?s:0}
function tscore(a,b,loc){var A=toks(a),B=toks(b);if(!A.length||!B.length)return 0;if(A.join(' ')===B.join(' '))return 1;
 var used=[],m=0;A.forEach(function(w){var bi=-1,bs=0;B.forEach(function(x,k){if(used[k])return;var s=wsim(w,x);if(s>bs){bs=s;bi=k}});if(bi>-1){used[bi]=1;m+=bs}});
 var mn=Math.min(A.length,B.length),sj=m/(A.length+B.length-m),cov=m/mn*Math.min(1,0.5+0.25*mn),ch=sim(A.slice().sort().join(' '),B.slice().sort().join(' '));
 var r=0.5*sj+0.3*cov+0.2*ch;if(loc)r=Math.max(r,0.9*(m/mn));return Math.min(1,r)}
function days(s){var p=s.split('-').map(Number);return Date.UTC(p[0],p[1]-1,p[2])/864e5}
function pc(x){return Math.round(x*100)+'%'}
function score(l,f){var t=tscore(l.name,f.name),d=tscore(l.desc,f.desc),lo=tscore(l.loc,f.loc,true),c=l.cat===f.cat?1:0.5*sim(l.cat,f.cat);
 var base=(t*0.45+d*0.25+lo*0.20+c*0.10)*100,gap=days(f.date)-days(l.date),dt,adj=0,flag='';
 if(gap<0){dt=0;base*=0.6;flag='Found '+(-gap)+' day(s) BEFORE it was lost, so this is unlikely (score reduced 40%)'}
 else if(gap<=3){dt=1;adj=8;flag=(gap===0?'Same day':'Found '+gap+' day(s) after loss')+' (+8 boost)'}
 else{dt=Math.max(0,1-(gap-3)/14);adj=-Math.min(15,(gap-3)*0.75);flag='Found '+gap+' days after loss (small penalty)'}
 return {t:t,d:d,lo:lo,c:c,dt:dt,flag:flag,bad:gap<0,total:Math.max(0,Math.min(100,base+adj))}}
var mcb=null;
function modal(t,h,ok,cb){$('#mt').textContent=t;$('#mb').innerHTML=h;$('#mok').textContent=ok;mcb=cb;$('#mdl').classList.add('show');var f=$('#mb input,#mb textarea');if(f)f.focus()}
function mclose(){$('#mdl').classList.remove('show');mcb=null}
function doImport(){var d;try{d=JSON.parse($('#bk').value)}catch(e){return toast('Invalid JSON: '+e.message,false)}
 var its=Array.isArray(d)?d:d&&d.items,hs=(d&&d.hist)||[];if(!Array.isArray(its))return toast('JSON must contain an items list.',false);
 var seen={},ok=[],bad=0;its.forEach(function(i){if(!i||typeof i!=='object'){bad++;return}
  var o={id:cl(i.id),type:i.type,name:cl(i.name),cat:cl(i.cat),loc:cl(i.loc),date:cl(i.date),desc:cl(i.desc),cn:cl(i.cn),ci:cl(i.ci),status:i.status};
  if(!/^[LF]\d{3,}$/.test(o.id)||seen[o.id]||(o.type!=='Lost'&&o.type!=='Found')||o.id[0]!==o.type[0]||!o.name||!o.cat||!o.loc||!o.desc||!validDate(o.date)||(o.status!=='Active'&&o.status!=='Recovered')){bad++;return}
  if(typeof i.img==='string'&&/^data:image\/(jpeg|png|webp|gif);base64,/.test(i.img))o.img=i.img;
  seen[o.id]=1;ok.push(o)});
 if(!ok.length)return toast('No valid records found in the JSON.',false);
 var hh=Array.isArray(hs)?hs.filter(function(h){return h&&seen[cl(h.id)]}).map(function(h){return {id:cl(h.id),name:cl(h.name),type:h.type==='Found'?'Found':'Lost',by:cl(h.by),vn:cl(h.vn),date:cl(h.date)}}):[];
 modal('Import records','<p>Replace the current '+S.items.length+' records with <b>'+ok.length+'</b> imported records?'+(bad?' ('+bad+' invalid skipped.)':'')+' This cannot be undone.</p>','Replace and import',function(){S.items=ok;S.hist=hh;sv();toast('Imported '+ok.length+' records.')})}
 
function label(p){return p>=S.cfg.strong?["Strong Possible Match","strong"]:p>=S.cfg.mod?["Moderate Possible Match","mod"]:p>=S.cfg.weak?["Weak Possible Match","weak"]:null}

function fill(sel,all){sel.innerHTML=(all?'<option value="">All</option>':"")+CATS.map(function(c){return "<option>"+esc(c)+"</option>"}).join("")}
function tab(n){TABS.forEach(function(t){$("#t-"+t[0]).classList.toggle("hide",t[0]!==n);});
 [].forEach.call($("#nav").children,function(b){b.classList.toggle("on",b.dataset.t===n)});
 if(n==="items")renderList();if(n==="pic")renderPics();if(n==="hist")renderHist();if(n==="admin")renderAdmin();if(n==="match")$("#matches").innerHTML=""}

function resetForm(){editId=null;$("#f").reset();$("#date").value=today();$("#type").disabled=false;$("#regTitle").textContent="Register item";$("#saveBtn").textContent="Save item";$("#cancelBtn").classList.add("hide")}
function saveItem(){
 var o={type:$("#type").value,name:cl($("#name").value),cat:$("#cat").value,loc:cl($("#loc").value),date:cl($("#date").value),desc:cl($("#desc").value),cn:cl($("#cn").value),ci:cl($("#ci").value)};
 if(!o.name||!o.loc||!o.desc||!o.date||!o.cn||!o.ci)return toast("All fields, including contact details, are required.",false);
 if(o.cn.length<2)return toast("Enter the contact person's name.",false);
 var dg=o.ci.replace(/\D/g,"");if(!(/^[^\s@]+@[^\s@]+\.[^\s@]{2,}$/.test(o.ci)||(/^\+?[\d\s\-()]+$/.test(o.ci)&&dg.length>=7&&dg.length<=15)))return toast("Contact must be a valid email or phone number.",false);
 if(o.name.length<2)return toast("Item name is too short.",false);
 if(!validDate(o.date))return toast("Enter a valid date that is not in the future.",false);
 var dup=S.items.some(function(i){return i.id!==editId&&i.type===o.type&&i.status==="Active"&&cl(i.name).toLowerCase()===o.name.toLowerCase()&&cl(i.loc).toLowerCase()===o.loc.toLowerCase()&&i.date===o.date});
 if(dup)return toast("Duplicate record: same item, place and date already exists.",false);
 if(editId){if(!admin)return toast("Admin login required to update.",false);
  var it=S.items.filter(function(i){return i.id===editId})[0];if(it){it.name=o.name;it.cat=o.cat;it.loc=o.loc;it.date=o.date;it.desc=o.desc;it.cn=o.cn;it.ci=o.ci}
  toast("Item "+editId+" updated.")}
 else{o.id=nextId(o.type);o.status="Active";S.items.push(o);toast("Registered "+o.type+" item "+o.id+".")}
 sv();resetForm();if(editId===null&&$("#t-reg").classList.contains("hide")===false){}
}
function renderList(){
 var q=cl($("#q").value).toLowerCase(),fc=$("#fc").value,ft=$("#ft").value,fs=$("#fs").value;
 var r=S.items.filter(function(i){return(!q||i.id.toLowerCase().indexOf(q)>-1||i.name.toLowerCase().indexOf(q)>-1)&&(!fc||i.cat===fc)&&(!ft||i.type===ft)&&(!fs||i.status===fs)});
 if(!r.length){$("#list").innerHTML='<p class="mu">No matching records found.</p>';return}
 $("#list").innerHTML="<table><tr><th>ID</th><th>Type</th><th>Item</th><th>Category</th><th>Location</th><th>Date</th><th>Status</th><th></th></tr>"+r.map(function(i){
  return "<tr><td>"+esc(i.id)+"</td><td>"+i.type+"</td><td>"+thumb(i)+"<b>"+esc(i.name)+"</b><br><span class='mu'>"+esc(i.desc)+"</span>"+(admin?"<br><span class='mu'>Contact: "+esc(i.cn||"—")+" · "+esc(i.ci||"—")+"</span>":"")+"</td><td>"+esc(i.cat)+"</td><td>"+esc(i.loc)+"</td><td>"+i.date+"</td><td><span class='tag "+(i.status==="Recovered"?"rec":"")+"'>"+i.status+"</span></td><td>"+
  (i.status==="Active"?"<button class='btn s' data-a='rec' data-id='"+i.id+"'>Recovered</button> ":"")+
  (admin?"<button class='btn s' data-a='edit' data-id='"+i.id+"'>Edit</button> <button class='btn s d' data-a='del' data-id='"+i.id+"'>Delete</button>":"")+"</td></tr>"}).join("")+"</table>"}
function markRec(id){var it=S.items.filter(function(i){return i.id===id})[0];if(!it||it.status==="Recovered")return;
 modal('Mark '+it.id+' as recovered','<label>Recovered by (name or roll no.) *</label><input id="rb" maxlength="60"><label style="margin-top:8px">Verification notes / ID check *</label><textarea id="rv" rows="3" maxlength="200" placeholder="e.g. Checked student ID card; described contents correctly"></textarea>','Confirm recovery',function(){var by=cl($('#rb').value),vn=cl($('#rv').value);
  if(by.length<2){toast('Enter who recovered the item.',false);return false}
  if(vn.length<5){toast('Verification notes / ID check are required.',false);return false}
  it.status='Recovered';S.hist.push({id:it.id,name:it.name,type:it.type,by:by,vn:vn,date:today()});sv();renderList();toast(it.id+' marked as recovered.')});
 }
function renderHist(){$("#hist").innerHTML=S.hist.length?"<table><tr><th>ID</th><th>Item</th><th>Type</th><th>Recovered by</th><th>Date</th><th>Verification</th></tr>"+S.hist.map(function(h){return "<tr><td>"+esc(h.id)+"</td><td>"+esc(h.name)+"</td><td>"+h.type+"</td><td>"+esc(h.by)+"</td><td>"+esc(h.date)+"</td><td>"+esc(h.vn||"—")+"</td></tr>"}).join("")+"</table>":'<p class="mu">No items recovered yet.</p>'}
function runMatch(){
 var L=S.items.filter(function(i){return i.type==="Lost"&&i.status==="Active"}),F=S.items.filter(function(i){return i.type==="Found"&&i.status==="Active"}),res=[];
 L.forEach(function(l){F.forEach(function(f){var s=score(l,f),lb=label(s.total);if(lb)res.push({l:l,f:f,s:s,lb:lb})})});
 res.sort(function(a,b){return b.s.total-a.s.total});
 if(!res.length){$("#matches").innerHTML='<div class="card mu">No possible matches found (score below '+S.cfg.weak+'%, or no active Lost/Found items).</div>';return}
 $("#matches").innerHTML=res.map(function(m,i){var p=m.s.total.toFixed(1);return '<div class="card"><b>#'+(i+1)+' &nbsp;'+p+'%</b> <span class="tag '+m.lb[1]+'">'+m.lb[0]+'</span><div class="bar"><i style="width:'+p+'%"></i></div>'+
 '<div class="grid"><div>'+thumb(m.l)+'<span class="mu">Lost '+esc(m.l.id)+'</span><br><b>'+esc(m.l.name)+'</b><br>'+esc(m.l.loc)+" · "+m.l.date+'</div><div>'+thumb(m.f)+'<span class="mu">Found '+esc(m.f.id)+'</span><br><b>'+esc(m.f.name)+'</b><br>'+esc(m.f.loc)+" · "+m.f.date+'</div></div>'+
 '<div class="mu" style="margin-top:6px">Title '+pc(m.s.t)+' · Description '+pc(m.s.d)+' · Location '+pc(m.s.lo)+' · Category '+pc(m.s.c)+' · Date proximity '+pc(m.s.dt)+'</div><div style="margin-top:4px;font-size:13px;color:var(--'+(m.s.bad?'er':'ok')+')">'+esc(m.s.flag)+'</div></div>'}).join("")}
function renderAdmin(){var b=$("#adminBox");
 if(!admin){b.innerHTML='<h3 style="margin-top:0">Admin login</h3><p class="mu">Admins can edit and delete records. Default PIN: 1234 (change it after logging in).</p><div class="row"><div><label>PIN</label><input id="pin" type="password" maxlength="12"></div><button class="btn p" data-a="login">Login</button></div>';return}
 b.innerHTML='<h3 style="margin-top:0">Admin settings</h3><div class="grid"><div><label>Strong match from (%)</label><input id="cs" type="number" min="1" max="100" value="'+S.cfg.strong+'"></div><div><label>Moderate match from (%)</label><input id="cm" type="number" min="1" max="100" value="'+S.cfg.mod+'"></div><div><label>Weak match from (%)</label><input id="cw" type="number" min="1" max="100" value="'+S.cfg.weak+'"></div><div><label>New PIN (optional, 4-12 chars)</label><input id="np" type="password" maxlength="12"></div></div><div class="row" style="margin-top:12px"><button class="btn p" data-a="cfg">Save settings</button><button class="btn" data-a="logout">Logout</button></div><div class="bk"><h3 style="margin-top:0">Backup</h3><p class="mu">Export your records as JSON and keep them safe in case browser storage is cleared. To restore, paste the JSON below or choose a file, then click Import.</p><div class="row"><button class="btn" data-a="exp">Export JSON</button><button class="btn" data-a="cp">Copy</button><button class="btn" data-a="imp">Import JSON</button></div><div style="margin-top:8px"><input id="impf" type="file" accept=".json,application/json"></div><textarea id="bk" rows="6" style="margin-top:8px;font-family:monospace;font-size:12px"></textarea></div>'}
var pdata=null;
function thumb(i){return i.img?"<img class='th' alt='Picture of "+esc(i.name)+"' src='"+i.img+"' data-a='pz' data-id='"+esc(i.id)+"'>":""}
function readImg(file,cb){
 if(!/^image\//.test(file.type))return cb(null,"Please choose an image file.");
 if(file.size>15*1024*1024)return cb(null,"Image is too large (max 15 MB).");
 var r=new FileReader();r.onerror=function(){cb(null,"Could not read that file.")};
 r.onload=function(){var im=new Image();im.onerror=function(){cb(null,"Could not read that image.")};
  im.onload=function(){var m=640,k=Math.min(1,m/Math.max(im.width,im.height)),c=document.createElement("canvas");c.width=Math.max(1,Math.round(im.width*k));c.height=Math.max(1,Math.round(im.height*k));
   var x=c.getContext("2d");x.fillStyle="#fff";x.fillRect(0,0,c.width,c.height);x.drawImage(im,0,0,c.width,c.height);cb(c.toDataURL("image/jpeg",0.72))};
  im.src=r.result};
 r.readAsDataURL(file)}
function renderPics(){
 var sel=$("#pi"),cur=sel.value;
 sel.innerHTML=S.items.length?S.items.map(function(i){return '<option value="'+esc(i.id)+'">'+esc(i.id)+" · "+i.type+" · "+esc(i.name)+(i.img?" 📷":"")+"</option>"}).join(""):'<option value="">No items registered yet</option>';
 if(cur&&S.items.some(function(i){return i.id===cur}))sel.value=cur;
 var w=S.items.filter(function(i){return i.img});
 $("#pgal").innerHTML=w.length?w.map(function(i){return '<div class="card"><img alt="Picture of '+esc(i.name)+'" src="'+i.img+'" data-a="pz" data-id="'+esc(i.id)+'"><b>'+esc(i.name)+'</b><br><span class="tag '+(i.type==="Found"?"rec":"")+'">'+i.type+'</span> <span class="mu">'+esc(i.id)+' · '+esc(i.loc)+'</span><div style="margin-top:6px"><button class="btn s" data-a="pp" data-id="'+esc(i.id)+'">Replace</button>'+(admin?' <button class="btn s d" data-a="pr" data-id="'+esc(i.id)+'">Remove</button>':'')+'</div></div>'}).join(""):'<div class="card mu" style="grid-column:1/-1">No pictures attached yet. Pick an item above and attach one.</div>'}
function attachPic(){
 var id=$("#pi").value,it=S.items.filter(function(i){return i.id===id})[0];
 if(!it)return toast("Select an item first.",false);
 if(!pdata)return toast("Choose a picture first.",false);
 var old=it.img;it.img=pdata;
 if(!sv()){if(old)it.img=old;else delete it.img;return toast("Browser storage is full. Remove some pictures or export a backup.",false)}
 pdata=null;$("#pf").value="";$("#pprev").innerHTML="";renderPics();toast("Picture "+(old?"replaced":"attached")+" for "+id+".")}
document.addEventListener("change",function(e){if(e.target.id!=="pf")return;var f=e.target.files[0];pdata=null;$("#pprev").innerHTML="";if(!f)return;
 readImg(f,function(d,err){if(err){e.target.value="";return toast(err,false)}pdata=d;$("#pprev").innerHTML='<img alt="Preview" src="'+d+'">'})});
document.addEventListener("click",function(e){var a=e.target.dataset&&e.target.dataset.a,id=e.target.dataset&&e.target.dataset.id;if(!a)return;
 var it=S.items.filter(function(i){return i.id===id})[0];
 if(a==="pz"&&it&&it.img)modal(it.id+" · "+it.name,'<img class="zoom" alt="Picture of '+esc(it.name)+'" src="'+it.img+'"><p class="mu" style="margin-bottom:0">'+it.type+' · '+esc(it.loc)+' · '+it.date+'</p>',"Close",null);
 else if(a==="pp"&&it){$("#pi").value=id;$("#pf").click();$("#pi").scrollIntoView({block:"center"})}
 else if(a==="pr"&&it&&admin)modal("Remove picture?","<p>Remove the picture from <b>"+esc(it.id)+" – "+esc(it.name)+"</b>?</p>","Remove",function(){delete it.img;sv();renderPics();renderList();toast("Picture removed.")})});

function seed(){var d=today();return [
 {id:"L001",type:"Lost",name:"Black Laptop Bag",cat:"Bags",loc:"Library",date:d,desc:"Black backpack with Dell laptop and blue charger",status:"Active"},
 {id:"F001",type:"Found",name:"Black Backpack",cat:"Bags",loc:"Library Reading Hall",date:d,desc:"Black bag containing a laptop and a blue charger",status:"Active"},
 {id:"L002",type:"Lost",name:"Water Bottle",cat:"Accessories",loc:"Cafeteria",date:d,desc:"Steel silver bottle with a sticker",status:"Active"},
 {id:"F002",type:"Found",name:"Student ID Card",cat:"ID & Cards",loc:"Block A",date:d,desc:"ID card with red lanyard",status:"Active"}]}

document.addEventListener("click",function(e){var a=e.target.dataset&&e.target.dataset.a;if(!a)return;var id=e.target.dataset.id;
 if(a==="rec")markRec(id);
 else if(a==="del"){if(!admin)return;var di=S.items.filter(function(i){return i.id===id})[0];if(di)modal('Delete record?','<p>Delete <b>'+esc(di.id)+' – '+esc(di.name)+'</b>? This cannot be undone. Export a backup first if unsure.</p>','Delete',function(){S.items=S.items.filter(function(i){return i.id!==id});sv();renderList();toast('Deleted '+id+'.')})}
 else if(a==="edit"){var it=S.items.filter(function(i){return i.id===id})[0];if(!it)return;editId=id;tab("reg");$("#type").value=it.type;$("#type").disabled=true;$("#name").value=it.name;$("#cat").value=it.cat;$("#loc").value=it.loc;$("#date").value=it.date;$("#desc").value=it.desc;$("#cn").value=it.cn||"";$("#ci").value=it.ci||"";$("#regTitle").textContent="Update item "+id;$("#saveBtn").textContent="Update item";$("#cancelBtn").classList.remove("hide")}
 else if(a==="exp"){var t=$("#bk");t.value=JSON.stringify({version:1,exported:today(),items:S.items,hist:S.hist},null,2);t.select();toast("Exported below. Copy it and save it in a .json file.")}
 else if(a==="cp"){var t2=$("#bk");t2.select();var cok=false;try{cok=document.execCommand("copy")}catch(x){}toast(cok?"Copied to clipboard.":"Press Ctrl+C to copy the selected text.")}
 else if(a==="imp")doImport();
 else if(a==="login"){if($("#pin").value===S.cfg.pin){admin=true;toast("Admin logged in.");renderAdmin()}else toast("Wrong PIN.",false)}
 else if(a==="logout"){admin=false;renderAdmin()}
 else if(a==="cfg"){var s=+$("#cs").value,m=+$("#cm").value,w=+$("#cw").value,np=$("#np").value;
  if(!(s<=100&&s>m&&m>w&&w>=1))return toast("Thresholds must satisfy 100 ≥ strong > moderate > weak ≥ 1.",false);
  if(np&&np.length<4)return toast("PIN must be at least 4 characters.",false);
  S.cfg.strong=s;S.cfg.mod=m;S.cfg.weak=w;if(np)S.cfg.pin=np;sv();toast("Settings saved.");renderAdmin()}});

(function init(){
 S.items=ld("clf_items",null);if(!Array.isArray(S.items)){S.items=seed()}
 S.hist=ld("clf_hist",[]);var c=ld("clf_cfg",null);if(c&&typeof c==="object")for(var k in c)S.cfg[k]=c[k];
 $("#nav").innerHTML=TABS.map(function(t){return '<button data-t="'+t[0]+'">'+t[1]+"</button>"}).join("");
 $("#nav").addEventListener("click",function(e){if(e.target.dataset.t){if(e.target.dataset.t!=="reg")resetForm();tab(e.target.dataset.t)}});
 fill($("#cat"),false);fill($("#fc"),true);$("#date").max=today();$("#date").value=today();
 $("#saveBtn").onclick=saveItem;
 $("#mok").onclick=function(){if(mcb&&mcb()===false)return;mclose()};$("#mno").onclick=mclose;
 document.addEventListener("keydown",function(e){if(e.key==="Escape")mclose()});
 document.addEventListener("change",function(e){if(e.target.id!=="impf"||!e.target.files[0])return;var r=new FileReader();r.onload=function(){$("#bk").value=String(r.result);toast("File loaded. Click Import JSON.")};r.onerror=function(){toast("Could not read file.",false)};r.readAsText(e.target.files[0])});$("#cancelBtn").onclick=function(){resetForm()};$("#runMatch").onclick=runMatch;$("#pAttach").onclick=attachPic;
 ["q","fc","ft","fs"].forEach(function(i){$("#"+i).addEventListener("input",renderList)});
 sv();tab("reg");
})();
</script>
</body>
</html>
