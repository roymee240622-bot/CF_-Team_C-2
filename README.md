<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>ติดตามการยืนยันยอดบัญชีเงินฝากธนาคาร</title>
<style>
:root{--bg:#f6f7f9;--card:#fff;--tx:#1b2430;--mu:#6b7683;--bd:#dfe3e8;--ac:#1f5fbf;--ok:#1a7f4b;--okb:#e0f3e8;--wt:#9a6700;--wtb:#fff1cc;--rd:#b42318;--rdb:#fde3e0;--gy:#59636e;--gyb:#eceff2;--bl:#1f5fbf;--blb:#e3edfb;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px);color-scheme:light}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#14171c;--card:#1d222a;--tx:#e8ebef;--mu:#98a2ae;--bd:#2f3640;--ac:#6ea4f5;--ok:#5fd394;--okb:#16352a;--wt:#f0c050;--wtb:#3a3014;--rd:#ff8f84;--rdb:#3d1f1c;--gy:#aab3bd;--gyb:#272d36;--bl:#8db8f8;--blb:#1b2c47;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#14171c;--card:#1d222a;--tx:#e8ebef;--mu:#98a2ae;--bd:#2f3640;--ac:#6ea4f5;--ok:#5fd394;--okb:#16352a;--wt:#f0c050;--wtb:#3a3014;--rd:#ff8f84;--rdb:#3d1f1c;--gy:#aab3bd;--gyb:#272d36;--bl:#8db8f8;--blb:#1b2c47;color-scheme:dark}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--tx);font-family:"Sarabun","Noto Sans Thai",system-ui,sans-serif;font-size:15px;line-height:1.5}
.wrap{max-width:1100px;margin:0 auto;padding:20px 16px 60px}
h1{font-size:22px;margin:0 0 4px}
.sub{color:var(--mu);margin:0 0 18px}
.stats{display:grid;grid-template-columns:repeat(auto-fit,minmax(130px,1fr));gap:10px;margin-bottom:16px}
.stat{background:var(--card);border:1px solid var(--bd);border-radius:10px;padding:10px 12px;cursor:pointer}
.stat b{display:block;font-size:22px}
.stat span{font-size:13px;color:var(--mu)}
.stat.on{outline:2px solid var(--ac)}
.bar{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:16px}
input,button,select{font:inherit;color:var(--tx)}
input[type=text],input[type=date]{background:var(--card);border:1px solid var(--bd);border-radius:8px;padding:7px 10px;min-width:0}
input[type=date]{width:100%}
.bar input{flex:1;min-width:160px}
button{background:var(--ac);color:#fff;border:0;border-radius:8px;padding:8px 14px;cursor:pointer}
button.ghost{background:transparent;color:var(--ac);border:1px solid var(--bd)}
button.x{background:transparent;color:var(--rd);padding:4px 8px}
.cust{background:var(--card);border:1px solid var(--bd);border-radius:12px;margin-bottom:14px;overflow:hidden}
.ch{display:flex;align-items:center;gap:8px;padding:12px 14px;border-bottom:1px solid var(--bd);flex-wrap:wrap}
.ch h2{margin:0;font-size:17px;flex:1}
.ch small{color:var(--mu)}
.scroll{overflow-x:auto}
table{border-collapse:collapse;width:100%;min-width:860px}
th,td{padding:8px 10px;text-align:left;border-bottom:1px solid var(--bd);vertical-align:middle}
th{font-size:13px;color:var(--mu);font-weight:600;background:var(--bg)}
td.bk{min-width:170px}
td.bk input{width:100%}
.badge{display:inline-block;padding:2px 10px;border-radius:99px;font-size:13px;white-space:nowrap}
.s0{background:var(--gyb);color:var(--gy)}.s1{background:var(--wtb);color:var(--wt)}.s2{background:var(--blb);color:var(--bl)}.s3{background:var(--wtb);color:var(--wt)}.s4{background:var(--okb);color:var(--ok)}
.late{color:var(--rd);font-size:12px;display:block}
.add{padding:10px 14px}
.empty{text-align:center;color:var(--mu);padding:40px 10px}
.ai{padding:14px}.ai input[type=file]{width:100%;padding:18px;border:2px dashed var(--bd);border-radius:10px;background:var(--bg)}.ai.drag input[type=file]{border-color:var(--ac)}.sum{font-size:17px;margin:12px 0 6px}.sum b{color:var(--ac)}.fl{margin:6px 0 12px;padding-left:20px}.fl small{color:var(--mu)}
.ups{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:10px;padding:14px 14px 0}.up{border:2px dashed var(--bd);border-radius:10px;padding:12px;background:var(--bg)}.up.drag{border-color:var(--ac)}.up b{display:block}.up small{color:var(--mu);display:block;margin-bottom:8px}.up input[type=file]{width:100%;font-size:13px}.cin{padding:14px 14px 0;display:flex;gap:8px;align-items:center;flex-wrap:wrap}.cin input{flex:1;min-width:200px}.ai{padding:14px}td.bk select{margin-top:4px;background:var(--card);border:1px solid var(--bd);border-radius:8px;padding:3px 6px;font-size:13px}.sum{font-size:17px;margin:4px 0 6px}.sum b{color:var(--ac)}.fl{margin:6px 0 12px;padding-left:20px}
</style>
</head>
<body>
<div class="wrap">
  <h1>ติดตามการยืนยันยอดบัญชีเงินฝากธนาคาร</h1>
  <p class="sub">ลูกค้า (สหกรณ์) 1 ราย มีได้หลายหน่วยงาน (ธนาคาร สหกรณ์ เงินลงทุน) · บันทึกวันที่แต่ละขั้นตอน ระบบสรุปสถานะให้อัตโนมัติ · ข้อมูลเก็บไว้ในเบราว์เซอร์ของคุณ</p>
  <div class="cust" id="aiBox" style="display:none"><div class="ch"><h2>อ่านไฟล์อัตโนมัติ</h2><small>อ่านเฉพาะคอลัมน์ชื่อหน่วยงาน · PDF, รูปภาพ, Excel/CSV, txt</small></div>
  <div class="cin"><label for="custIn">ลูกค้า (สหกรณ์):</label><input type="text" id="custIn" list="custList" placeholder="เว้นว่างได้ ระบบจะอ่านชื่อสหกรณ์จากไฟล์"><datalist id="custList"></datalist></div>
  <div class="ups">
   <div class="up" data-t="bank"><b>1. ไฟล์ธนาคาร</b><small>เงินฝากธนาคาร</small><input type="file" multiple accept=".pdf,.png,.jpg,.jpeg,.webp,.gif,.xlsx,.xls,.csv,.txt"></div>
   <div class="up" data-t="coop"><b>2. ไฟล์สหกรณ์</b><small>เงินฝากที่สหกรณ์อื่น</small><input type="file" multiple accept=".pdf,.png,.jpg,.jpeg,.webp,.gif,.xlsx,.xls,.csv,.txt"></div>
   <div class="up" data-t="inv"><b>3. เงินลงทุน</b><small>หลักทรัพย์ หรือธนาคาร</small><input type="file" multiple accept=".pdf,.png,.jpg,.jpeg,.webp,.gif,.xlsx,.xls,.csv,.txt"></div>
  </div><div class="ai" id="aiOut"></div></div>
  <div class="stats" id="stats"></div>
  <div class="bar">
    <input type="text" id="newCust" placeholder="ชื่อลูกค้าใหม่">
    <button id="addCust">+ เพิ่มลูกค้า</button>
    <input type="text" id="q" placeholder="ค้นหาลูกค้า / หน่วยงาน">
  </div>
  <div id="list"></div>
</div>
<script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
<script>
var KEY="bankconfirm-v1",data=[],filter=-1,query="";
var LABEL=["ยังไม่ส่งลูกค้า","รอลูกค้าส่งกลับ","รอส่งออกภายนอก","รอภายนอกตอบกลับ","เสร็จสิ้น"];
function load(){try{var r=localStorage.getItem(KEY);if(r)data=JSON.parse(r)||[]}catch(e){data=[]}}
function save(){try{localStorage.setItem(KEY,JSON.stringify(data))}catch(e){}}
function uid(){return Math.random().toString(36).slice(2,9)}
function esc(s){return String(s==null?"":s).replace(/[&<>"]/g,function(c){return{"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c]})}
function status(b){if(b.backExt)return 4;if(b.sentExt)return 3;if(b.backCust)return 2;if(b.sentCust)return 1;return 0}
function days(d){if(!d)return 0;return Math.floor((Date.now()-new Date(d).getTime())/864e5)}
function late(b){var s=status(b),d=s==1?days(b.sentCust):s==3?days(b.sentExt):0;return d>=14?"ค้างมาแล้ว "+d+" วัน":""}
function render(){
  var cnt=[0,0,0,0,0],total=0;
  data.forEach(function(c){c.banks.forEach(function(b){cnt[status(b)]++;total++})});
  var h='<div class="stat'+(filter==-1?' on':'')+'" data-f="-1"><b>'+total+'</b><span>ทั้งหมด</span></div>';
  for(var i=0;i<5;i++)h+='<div class="stat'+(filter==i?' on':'')+'" data-f="'+i+'"><b>'+cnt[i]+'</b><span>'+LABEL[i]+'</span></div>';
  document.getElementById("stats").innerHTML=h;
  var out="",q=query.toLowerCase();
  data.forEach(function(c){
    var cm=c.name.toLowerCase().indexOf(q)>-1;
    var rows=c.banks.filter(function(b){
      return (filter==-1||status(b)==filter)&&(!q||cm||b.bank.toLowerCase().indexOf(q)>-1)});
    if((filter!=-1||q)&&!rows.length)return;
    var done=c.banks.filter(function(b){return status(b)==4}).length;
    out+='<div class="cust"><div class="ch"><h2>'+esc(c.name)+'</h2><small>เสร็จ '+done+'/'+c.banks.length+' รายการ</small><button class="ghost" data-a="addbank" data-c="'+c.id+'">+ รายการ</button><button class="x" data-a="delcust" data-c="'+c.id+'">ลบลูกค้า</button></div>';
    if(rows.length){
      out+='<div class="scroll"><table><tr><th>1. ชื่อหน่วยงาน / ประเภท</th><th>2. ส่งให้ลูกค้า</th><th>3. ลูกค้าส่งกลับ</th><th>4. ส่งออกภายนอก</th><th>5. ภายนอกส่งกลับ</th><th>สถานะ</th><th></th></tr>';
      rows.forEach(function(b){
        var s=status(b),k='data-c="'+c.id+'" data-b="'+b.id+'"';
        out+='<tr><td class="bk"><input type="text" value="'+esc(b.bank)+'" placeholder="ชื่อหน่วยงาน" data-k="bank" '+k+'>'+typeSel(b,k)+'</td>';
        ["sentCust","backCust","sentExt","backExt"].forEach(function(f){out+='<td><input type="date" value="'+esc(b[f])+'" data-k="'+f+'" '+k+'></td>'});
        out+='<td><span class="badge s'+s+'">'+LABEL[s]+'</span><span class="late">'+late(b)+'</span></td><td><button class="x" data-a="delbank" '+k+'>ลบ</button></td></tr>';
      });
      out+='</table></div>';
    }else out+='<div class="empty">ยังไม่มีรายการ กด + รายการ เพื่อเพิ่ม</div>';
    out+='</div>';
  });
  document.getElementById("list").innerHTML=out||'<div class="empty">ยังไม่มีข้อมูล เพิ่มชื่อลูกค้าด้านบนเพื่อเริ่มต้น</div>';
}
function find(id){return data.filter(function(c){return c.id==id})[0]}
document.getElementById("addCust").onclick=function(){
  var i=document.getElementById("newCust"),n=i.value.trim();if(!n)return;
  data.push({id:uid(),name:n,banks:[{id:uid(),bank:"",type:"bank",sentCust:"",backCust:"",sentExt:"",backExt:""}]});
  i.value="";save();render();fillCustList()};
document.getElementById("newCust").onkeydown=function(e){if(e.key=="Enter")document.getElementById("addCust").click()};
document.getElementById("q").oninput=function(e){query=e.target.value.trim();render()};
document.getElementById("stats").onclick=function(e){var s=e.target.closest(".stat");if(!s)return;filter=+s.dataset.f;render()};
document.getElementById("list").onclick=function(e){
  var t=e.target.closest("button");if(!t)return;var c=find(t.dataset.c),a=t.dataset.a;
  if(a=="addbank")c.banks.push({id:uid(),bank:"",type:"bank",sentCust:"",backCust:"",sentExt:"",backExt:""});
  else if(a=="delcust"){if(!confirm("ลบลูกค้า "+c.name+" และธนาคารทั้งหมด?"))return;data=data.filter(function(x){return x!=c})}
  else if(a=="delbank"){if(!confirm("ลบรายการธนาคารนี้?"))return;c.banks=c.banks.filter(function(b){return b.id!=t.dataset.b})}
  save();render()};
document.getElementById("list").onchange=function(e){
  var t=e.target;if(!t.dataset.k)return;var c=find(t.dataset.c);
  c.banks.forEach(function(b){if(b.id==t.dataset.b)b[t.dataset.k]=t.value});
  save();render()};
var sampleFn=null,found=null,foundT="bank";
var TN={bank:"ธนาคาร",coop:"สหกรณ์",inv:"เงินลงทุน"};
var DESC={bank:"รายการเงินฝากธนาคาร (ชื่อหน่วยงานคือธนาคาร)",coop:"รายการเงินฝากหรือเงินให้ยืมที่สหกรณ์ลูกค้ามีอยู่กับสหกรณ์อื่น (ชื่อหน่วยงานคือสหกรณ์)",inv:"รายการเงินลงทุนในหลักทรัพย์หรือธนาคาร (ชื่อหน่วยงานคือผู้ออกหลักทรัพย์ ธนาคาร หรือกองทุน)"};
function typeSel(b,k){var t=b.type||"bank",h='<select data-k="type" '+k+'>';Object.keys(TN).forEach(function(x){h+='<option value="'+x+'"'+(x==t?' selected':'')+'>'+TN[x]+'</option>'});return h+'</select>'}
function mkPrompt(t,cust){return "คุณเป็นผู้ช่วยผู้สอบบัญชี ลูกค้าที่ตรวจสอบคือสหกรณ์ เอกสารที่แนบเป็น"+DESC[t]+" ให้อ่านเฉพาะคอลัมน์ที่เป็นชื่อหน่วยงานคู่ค้า (ไม่จำเป็นต้องเป็นธนาคาร) ไม่ต้องสนใจคอลัมน์อื่น เช่น ยอดเงิน วันที่ เลขที่บัญชี และให้ระบุชื่อสหกรณ์ลูกค้าเจ้าของข้อมูลจากหัวกระดาษ ชื่อไฟล์ หรือหัวตาราง"+(cust?" (ผู้ใช้ระบุว่าลูกค้าคือ "+cust+")":"")+" ตอบเป็น JSON เท่านั้น รูปแบบ {\"customer\":\"ชื่อสหกรณ์ลูกค้า หรือ null\",\"names\":[\"ชื่อหน่วยงาน\"],\"note\":\"หมายเหตุสั้นๆ ถ้ามี\"} ชื่อซ้ำให้รวมเป็นหนึ่ง ห้ามเดาข้อมูลที่ไม่มีในไฟล์ ข้อมูลจากไฟล์:"}
(async function(){try{if(window.claude)sampleFn=await claude.use("sample")}catch(e){}
 if(sampleFn)document.getElementById("aiBox").style.display="block"})();
function setAi(h){document.getElementById("aiOut").innerHTML=h}
function fillCustList(){document.getElementById("custList").innerHTML=data.map(function(c){return '<option value="'+esc(c.name)+'">'}).join("")}
async function prepare(files){
 var texts=[],imgs=[],lim=null;
 try{lim=await sampleFn.limits()}catch(e){}
 var maxImg=(lim&&lim.images&&lim.images.maxCount)||0;
 for(var i=0;i<files.length;i++){var f=files[i],n=f.name.toLowerCase();
  if(/\.(png|jpe?g|webp|gif)$/.test(n)){imgs.push(f);continue}
  if(/\.pdf$/.test(n)){
   if(!window.pdfjsLib)throw new Error("โหลดตัวอ่าน PDF ไม่ได้");
   pdfjsLib.GlobalWorkerOptions.workerSrc="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js";
   var pdf=await pdfjsLib.getDocument({data:await f.arrayBuffer()}).promise,t="";
   for(var p=1;p<=Math.min(pdf.numPages,30);p++){var pg=await pdf.getPage(p),tc=await pg.getTextContent();t+=tc.items.map(function(x){return x.str}).join(" ")+"\n"}
   if(t.replace(/\s/g,"").length>80){texts.push("[ไฟล์ "+f.name+"]\n"+t)}
   else if(maxImg){for(var q=1;q<=Math.min(pdf.numPages,8);q++){
     var pg2=await pdf.getPage(q),vp=pg2.getViewport({scale:1.5}),cv=document.createElement("canvas");
     cv.width=vp.width;cv.height=vp.height;
     await pg2.render({canvasContext:cv.getContext("2d"),viewport:vp}).promise;
     imgs.push(await new Promise(function(r){cv.toBlob(r,"image/jpeg",.85)}))}}
   continue}
  if(/\.(xlsx|xls|csv)$/.test(n)){
   if(!window.XLSX)throw new Error("โหลดตัวอ่าน Excel ไม่ได้");
   var wb=XLSX.read(await f.arrayBuffer());
   wb.SheetNames.forEach(function(s){texts.push("[ไฟล์ "+f.name+" / ชีต "+s+"]\n"+XLSX.utils.sheet_to_csv(wb.Sheets[s]))});continue}
  texts.push("[ไฟล์ "+f.name+"]\n"+await f.text())}
 if(imgs.length&&!maxImg)throw new Error("ส่งรูปให้ Claude ไม่ได้ในมุมมองนี้");
 return{text:texts.join("\n\n").slice(0,80000),imgs:imgs.slice(0,maxImg||0)}}
async function runAi(files,t){
 if(!files||!files.length)return;
 setAi('<p class="sub">กำลังอ่านไฟล์… อาจใช้เวลาสักครู่</p>');
 try{var pr=await prepare(files);
  if(!pr.text&&!pr.imgs.length)throw new Error("ไม่พบข้อมูลที่อ่านได้ในไฟล์");
  var opt={};if(pr.imgs.length)opt.images=pr.imgs;
  found=await sampleFn.json(mkPrompt(t,document.getElementById("custIn").value.trim())+"\n\n"+pr.text,opt);
  foundT=t;showFound();
 }catch(e){setAi('<p class="late">อ่านไฟล์ไม่สำเร็จ: '+esc(e&&e.code==="not_granted"?"ยังไม่ได้อนุญาตให้ใช้ Claude":(e&&(e.message||e.code))||e)+'</p>')}}
function foundNames(){var seen={},out=[];((found&&found.names)||[]).forEach(function(x){var n=String((x&&x.name)||x||"").trim();if(!n||seen[n.toLowerCase()])return;seen[n.toLowerCase()]=1;out.push(n)});return out}
function showFound(){
 var ns=foundNames(),cn=document.getElementById("custIn").value.trim()||(found&&found.customer?String(found.customer):"");
 var h='<p class="sum">ประเภท: <b>'+TN[foundT]+'</b> · พบ <b>'+ns.length+'</b> หน่วยงาน</p>';
 h+='<div class="cin" style="padding:0 0 8px"><label>ลูกค้า (สหกรณ์):</label><input type="text" id="resCust" list="custList" value="'+esc(cn)+'" placeholder="ไม่พบชื่อในไฟล์ กรุณากรอก"></div><ul class="fl">';
 ns.forEach(function(n){h+='<li>'+esc(n)+'</li>'});h+='</ul>';
 if(found&&found.note)h+='<p class="sub">หมายเหตุ: '+esc(found.note)+'</p>';
 if(ns.length)h+='<button id="impBtn">นำเข้าลงตารางติดตาม</button> ';
 h+='<small class="sub">AI อ่านจากไฟล์ ควรตรวจสอบความถูกต้องก่อนนำเข้า</small>';
 setAi(h)}
function importFound(){
 var ns=foundNames(),name=document.getElementById("resCust").value.trim();
 if(!name){alert("กรุณาระบุชื่อลูกค้า (สหกรณ์) ก่อนนำเข้า");return}
 var c=data.filter(function(x){return x.name.toLowerCase()==name.toLowerCase()})[0];
 if(!c){c={id:uid(),name:name,banks:[]};data.push(c)}
 ns.forEach(function(n){if(!c.banks.some(function(x){return x.bank.toLowerCase()==n.toLowerCase()&&(x.type||"bank")==foundT}))c.banks.push({id:uid(),bank:n,type:foundT,sentCust:"",backCust:"",sentExt:"",backExt:""})});
 save();render();fillCustList();setAi('<p class="sub">นำเข้า '+ns.length+' รายการ ให้ '+esc(name)+' แล้ว เลือกไฟล์ประเภทอื่นเพื่ออ่านต่อได้</p>')}
document.getElementById("aiOut").onclick=function(e){if(e.target.id=="impBtn")importFound()};
document.querySelectorAll(".up").forEach(function(el){
 var t=el.dataset.t;
 el.querySelector("input").onchange=function(e){runAi(e.target.files,t)};
 el.ondragover=function(e){e.preventDefault();el.classList.add("drag")};
 el.ondragleave=function(){el.classList.remove("drag")};
 el.ondrop=function(e){e.preventDefault();el.classList.remove("drag");runAi(e.dataTransfer.files,t)}});
load();render();fillCustList();
</script>
</body>
</html>
