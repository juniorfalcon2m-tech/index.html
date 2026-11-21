# index.html

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#17132f">
<meta name="description" content="Rate Me — positive, consent-based feedback with friends.">
<title>Rate Me — Be seen. Be celebrated.</title>
<style>
:root{--ink:#211d36;--muted:#77738c;--paper:#f7f5fb;--card:#fff;--purple:#7057e8;--pink:#f27cae;--line:#ebe8f3;--mint:#dff8ed;--shadow:0 12px 34px rgba(44,31,92,.08)}
*{box-sizing:border-box}body{margin:0;background:var(--paper);color:var(--ink);font:15px/1.5 Inter,system-ui,-apple-system,Segoe UI,sans-serif}
button,input,textarea,select{font:inherit}button{cursor:pointer}
.top{position:sticky;top:0;z-index:5;background:rgba(247,245,251,.92);backdrop-filter:blur(16px);border-bottom:1px solid var(--line)}
.topin{max-width:1100px;margin:auto;padding:12px 18px;display:flex;align-items:center;justify-content:space-between;gap:12px}
.brand{display:flex;align-items:center;gap:10px;font-weight:900;letter-spacing:-.7px;font-size:21px}.logo{width:37px;height:37px;border-radius:13px;background:linear-gradient(135deg,var(--purple),var(--pink));display:grid;place-items:center;color:white;font-weight:900;box-shadow:0 7px 16px #7057e844}
.topright{display:flex;align-items:center;gap:9px}.lang{border:1px solid var(--line);background:white;border-radius:12px;padding:8px;color:var(--ink)}
.wrap{max-width:1100px;margin:26px auto;padding:0 18px;display:grid;grid-template-columns:220px minmax(0,1fr) 245px;gap:20px}
.panel,.card{background:var(--card);border:1px solid var(--line);border-radius:21px;box-shadow:var(--shadow)}
.side{padding:17px;height:max-content;position:sticky;top:78px}.navbtn{display:flex;align-items:center;gap:12px;padding:12px;border-radius:13px;color:var(--muted);font-weight:700;cursor:pointer;margin:3px 0}.navbtn.active,.navbtn:hover{background:#f0edff;color:var(--purple)}.navicon{width:23px;text-align:center;font-size:18px}
.hero{padding:24px;border-radius:24px;background:linear-gradient(120deg,#282044,#5945a8 65%,#c16caa);color:white;position:relative;overflow:hidden;margin-bottom:16px}.hero:after{content:"";position:absolute;width:190px;height:190px;border:1px solid #ffffff33;border-radius:50%;right:-50px;top:-75px;box-shadow:0 0 0 24px #ffffff0c,0 0 0 50px #ffffff08}.hero h1{font-size:clamp(26px,4vw,38px);line-height:1.08;margin:0 0 9px;max-width:480px;letter-spacing:-1.3px}.hero p{color:#e6defd;margin:0;max-width:470px}.hero .pill{display:inline-block;margin-top:17px;background:#ffffff20;border:1px solid #ffffff3b;border-radius:30px;padding:6px 11px;font-size:12px;font-weight:800}
.composer{padding:17px;margin-bottom:16px}.row{display:flex;align-items:center;gap:11px}.avatar{width:42px;height:42px;border-radius:15px;background:linear-gradient(135deg,#ffd5e7,#cfc4ff);display:grid;place-items:center;font-weight:900;color:#51418d;flex-shrink:0}.avatar.small{width:35px;height:35px;border-radius:12px;font-size:13px}.grow{flex:1;min-width:0}.muted{color:var(--muted)}.field{width:100%;border:1px solid var(--line);background:#fbfaff;border-radius:13px;padding:12px;color:var(--ink);outline:none}.field:focus{border-color:#a99af7;box-shadow:0 0 0 3px #7057e81c}textarea.field{resize:vertical;min-height:82px;margin-top:12px}.compose-actions{display:flex;justify-content:space-between;align-items:center;margin-top:12px;gap:10px;flex-wrap:wrap}.btn{border:0;border-radius:13px;padding:10px 15px;background:var(--purple);color:white;font-weight:800;box-shadow:0 6px 15px #7057e833}.btn:hover{filter:brightness(1.05)}.btn.soft{background:#f0edff;color:var(--purple);box-shadow:none}.btn.ghost{background:white;border:1px solid var(--line);color:var(--ink);box-shadow:none}.sectionhead{display:flex;align-items:center;justify-content:space-between;margin:18px 2px 10px}.sectionhead h2{font-size:17px;margin:0;letter-spacing:-.3px}
.post{padding:17px;margin-bottom:14px}.posthead{display:flex;align-items:center;gap:10px}.postname{font-weight:850}.handle{font-size:12px;color:var(--muted)}.posttime{margin-left:auto;color:var(--muted);font-size:12px}.posttext{margin:14px 0;white-space:pre-wrap;overflow-wrap:anywhere}.tag{display:inline-block;border-radius:30px;padding:5px 9px;background:#f0edff;color:#6753cf;font-size:11px;font-weight:800}.actions{display:flex;gap:8px;border-top:1px solid var(--line);padding-top:12px;margin-top:12px}.action{border:0;background:transparent;color:var(--muted);font-weight:700;padding:7px 9px;border-radius:10px}.action:hover,.action.liked{background:#fff0f5;color:#e45d91}.ratebox{margin-top:13px;padding:14px;background:linear-gradient(135deg,#faf8ff,#fff6fa);border:1px solid #eee8ff;border-radius:16px}.ratebox h3{margin:0 0 5px;font-size:16px}.ratechoices{display:flex;gap:8px;flex-wrap:wrap;margin-top:12px}.choice{border:1px solid #e6defb;background:white;border-radius:12px;padding:8px 11px;color:#5f4ac6;font-weight:750}.choice.selected{background:#7057e8;color:white;border-color:#7057e8}.choice:disabled{opacity:.7;cursor:default}
.rightbox{padding:17px;margin-bottom:14px}.rightbox h3{margin:0 0 12px;font-size:15px}.person{display:flex;align-items:center;gap:9px;margin:12px 0}.person .grow{font-size:13px;font-weight:750}.trend{padding:10px 0;border-top:1px solid var(--line);font-size:13px}.trend b{display:block}.footnote{font-size:11px;color:var(--muted);line-height:1.5;margin-top:13px}
.empty{text-align:center;padding:35px 18px;color:var(--muted)}.empty strong{display:block;color:var(--ink);font-size:17px;margin-bottom:5px}
.toast{position:fixed;bottom:22px;left:50%;transform:translateX(-50%);background:#211d36;color:white;padding:11px 16px;border-radius:13px;box-shadow:var(--shadow);z-index:10;display:none;max-width:90%;text-align:center}
.modalback{position:fixed;inset:0;background:#17132f88;display:none;align-items:center;justify-content:center;padding:18px;z-index:20}.modal{background:white;border-radius:22px;padding:21px;width:min(100%,440px);box-shadow:0 20px 60px #17132f44}.modal h2{margin:0 0 8px}.modal .field{margin:7px 0}.modalfoot{display:flex;justify-content:flex-end;gap:8px;margin-top:12px}
.mobilebar{display:none}
@media(max-width:850px){.wrap{grid-template-columns:1fr;max-width:650px;margin:17px auto;padding-bottom:80px}.side,.rightcol{display:none}.mobilebar{display:flex;position:fixed;bottom:0;left:0;right:0;z-index:8;background:#ffffffed;backdrop-filter:blur(15px);border-top:1px solid var(--line);justify-content:space-around;padding:9px 5px calc(9px + env(safe-area-inset-bottom))}.mobilebar button{border:0;background:none;color:var(--muted);font-size:11px;font-weight:750;display:grid;gap:2px;justify-items:center}.mobilebar button span{font-size:20px}.mobilebar button.active{color:var(--purple)}}
@media(min-width:851px){.main{min-width:0}}
</style>
</head>
<body>
<header class="top"><div class="topin">
  <div class="brand"><div class="logo">R</div><span>rate me<span style="color:var(--pink)">.</span></span></div>
  <div class="topright"><select class="lang" id="language" aria-label="Choose language"><option value="en">English</option><option value="fr">Français</option><option value="es">Español</option><option value="ha">Hausa</option></select><button class="btn soft" id="profileBtn">My profile</button></div>
</div></header>
<div class="wrap">
  <aside class="side panel">
    <div class="navbtn active" data-view="home"><span class="navicon">⌂</span><span data-i18n="home">Home</span></div>
    <div class="navbtn" data-view="discover"><span class="navicon">✧</span><span data-i18n="discover">Discover</span></div>
    <div class="navbtn" data-view="ratings"><span class="navicon">♡</span><span data-i18n="ratings">Rate cards</span></div>
    <div class="navbtn" data-view="profile"><span class="navicon">◉</span><span data-i18n="profile">My profile</span></div>
    <div class="footnote">A kinder corner of the internet. Rate ideas, talents and good vibes — always with consent.</div>
  </aside>
  <main class="main">
    <section class="hero">
      <h1 data-i18n="heroTitle">Be seen. Be celebrated.</h1>
      <p data-i18n="heroText">Share your moments, cheer on your people, and collect good-vibe feedback.</p>
      <span class="pill" data-i18n="heroPill">✨ Your space to shine</span>
    </section>
    <section class="composer card">
      <div class="row"><div class="avatar" id="myAvatar">Y</div><div class="grow"><input id="displayName" class="field" maxlength="28" placeholder="Your display name" value="Your Name"></div></div>
      <textarea id="postInput" class="field" maxlength="400" placeholder="What would you like to share today?"></textarea>
      <div class="compose-actions"><span class="muted" style="font-size:12px">💜 Keep it kind. Max 400 characters.</span><button class="btn" id="postBtn">Share post</button></div>
    </section>
    <div class="sectionhead"><h2 id="feedTitle">Your community</h2><span class="tag" id="feedCount">DEMO FEED</span></div>
    <div id="feed"></div>
  </main>
  <aside class="rightcol">
    <section class="rightbox panel">
      <h3>🌟 People to cheer on</h3>
      <div class="person"><div class="avatar small">AM</div><div class="grow">Amara M.<div class="muted">Creative soul</div></div><button class="btn soft follow">Follow</button></div>
      <div class="person"><div class="avatar small">DK</div><div class="grow">David K.<div class="muted">Music lover</div></div><button class="btn soft follow">Follow</button></div>
      <div class="person"><div class="avatar small">ZB</div><div class="grow">Zee B.<div class="muted">Good energy</div></div><button class="btn soft follow">Follow</button></div>
    </section>
    <section class="rightbox panel">
      <h3>🔥 Community topics</h3>
      <div class="trend"><b>#ShowYourTalent</b><span class="muted">Share what you love doing</span></div>
      <div class="trend"><b>#GoodVibesOnly</b><span class="muted">Celebrate someone today</span></div>
      <div class="trend"><b>#RateMyIdea</b><span class="muted">Get kind, useful feedback</span></div>
      <p class="footnote">Demo content is stored only in this browser. It is not visible to other people yet.</p>
    </section>
  </aside>
</div>
<nav class="mobilebar"><button class="active" data-view="home"><span>⌂</span>Home</button><button data-view="discover"><span>✧</span>Discover</button><button data-view="ratings"><span>♡</span>Rate</button><button data-view="profile"><span>◉</span>Profile</button></nav>
<div class="toast" id="toast"></div>
<div class="modalback" id="modalBack"><div class="modal"><h2 id="modalTitle">Create a rate card</h2><p class="muted" id="modalDesc">Ask friends for positive feedback on something you choose.</p><input id="rateQuestion" class="field" maxlength="100" placeholder="Example: Rate my new logo idea"><input id="rateOption1" class="field" maxlength="35" value="Love it ✨"><input id="rateOption2" class="field" maxlength="35" value="Great start 💜"><input id="rateOption3" class="field" maxlength="35" value="Could improve 🌱"><div class="modalfoot"><button class="btn ghost" id="cancelModal">Cancel</button><button class="btn" id="createRate">Create card</button></div></div></div>
<script>
const translations={
 en:{home:"Home",discover:"Discover",ratings:"Rate cards",profile:"My profile",heroTitle:"Be seen. Be celebrated.",heroText:"Share your moments, cheer on your people, and collect good-vibe feedback.",heroPill:"✨ Your space to shine",share:"Share post",placeholder:"What would you like to share today?",community:"Your community",empty:"Nothing here yet",emptyText:"Be the first to share something positive.",like:"Like",comment:"Comment",rate:"Create rate card",profileTitle:"Your profile",discoverTitle:"Discover good vibes",rateTitle:"Community rate cards"},
 fr:{home:"Accueil",discover:"Découvrir",ratings:"Cartes d'avis",profile:"Mon profil",heroTitle:"Soyez vu. Soyez célébré.",heroText:"Partagez vos moments et encouragez votre communauté.",heroPill:"✨ Votre espace pour briller",share:"Publier",placeholder:"Que souhaitez-vous partager aujourd'hui ?",community:"Votre communauté",empty:"Rien ici pour le moment",emptyText:"Soyez le premier à partager quelque chose de positif.",like:"J'aime",comment:"Commenter",rate:"Créer une carte",profileTitle:"Votre profil",discoverTitle:"Découvrir",rateTitle:"Cartes d'avis"},
 es:{home:"Inicio",discover:"Descubrir",ratings:"Tarjetas",profile:"Mi perfil",heroTitle:"Déjate ver. Celebra tu esencia.",heroText:"Comparte momentos y anima a tu comunidad.",heroPill:"✨ Tu espacio para brillar",share:"Publicar",placeholder:"¿Qué quieres compartir hoy?",community:"Tu comunidad",empty:"Todavía no hay nada",emptyText:"Sé la primera persona en compartir algo positivo.",like:"Me gusta",comment:"Comentar",rate:"Crear tarjeta",profileTitle:"Tu perfil",discoverTitle:"Descubrir",rateTitle:"Tarjetas de opinión"},
 ha:{home:"Gida",discover:"Gano",ratings:"Katunan ra'ayi",profile:"Bayanan martaba",heroTitle:"A gan ka. A yaba maka.",heroText:"Raba lokutanka, ka ƙarfafa abokanka, ka sami kyakkyawan ra'ayi.",heroPill:"✨ Wurin haskaka kanka",share:"Raba rubutu",placeholder:"Me kake son rabawa yau?",community:"Al'ummarka",empty:"Babu komai tukuna",emptyText:"Ka fara da raba abu mai kyau.",like:"So",comment:"Sharhi",rate:"Ƙirƙiri kati",profileTitle:"Bayanan martaba",discoverTitle:"Gano abubuwa masu kyau",rateTitle:"Katunan ra'ayi"}
};
const starter=[
{id:1,name:"Amara M.",handle:"@amaracreates",initial:"A",time:"2h",text:"Finally shared my first digital illustration today! A little nervous, but proud of taking the leap. 🎨💜",likes:12,liked:false,tag:"#ShowYourTalent"},
{id:2,name:"David K.",handle:"@davidk",initial:"D",time:"4h",text:"Small reminder: your progress is still progress, even when nobody sees it. Keep going. 🌱",likes:8,liked:false,tag:"#GoodVibesOnly"}
];
let posts=JSON.parse(localStorage.getItem("rateme_posts")||"null")||starter;
let rateCards=JSON.parse(localStorage.getItem("rateme_rates")||"null")||[{id:101,name:"Zee B.",question:"Which colour fits this new project best?",options:["Lavender 💜","Sunset pink 🌸","Ocean blue 🌊"],votes:[8,5,3],voted:-1}];
let view="home",lang="en";
const $=id=>document.getElementById(id);
function save(){localStorage.setItem("rateme_posts",JSON.stringify(posts));localStorage.setItem("rateme_rates",JSON.stringify(rateCards))}
function toast(msg){$("toast").textContent=msg;$("toast").style.display="block";setTimeout(()=>$("toast").style.display="none",2400)}
function safe(s){return String(s).replace(/[&<>"']/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c]))}
function name(){return $("displayName").value.trim()||"Your Name"}
function initials(s){return s.split(/\s+/).map(x=>x[0]).join("").slice(0,2).toUpperCase()}
function setLanguage(v){lang=v;document.querySelectorAll("[data-i18n]").forEach(el=>{let k=el.dataset.i18n;if(translations[v][k])el.textContent=translations[v][k]});$("postInput").placeholder=translations[v].placeholder;$("postBtn").textContent=translations[v].share;render()}
function render(){
 const t=translations[lang];let list=posts;
 $("feedTitle").textContent=view==="profile"?t.profileTitle:view==="discover"?t.discoverTitle:view==="ratings"?t.rateTitle:t.community;
 if(view==="ratings"){ $("feed").innerHTML=rateCards.map(card=>`<article class="post card"><div class="posthead"><div class="avatar small">${safe(initials(card.name))}</div><div class="grow"><div class="postname">${safe(card.name)}</div><div class="handle">Community rate card</div></div></div><div class="ratebox"><h3>${safe(card.question)}</h3><div class="muted" style="font-size:12px">Choose one option — keep feedback respectful.</div><div class="ratechoices">${card.options.map((o,i)=>`<button class="choice ${card.voted===i?"selected":""}" data-rate="${card.id}" data-option="${i}" ${card.voted!==-1?"disabled":""}>${safe(o)}${card.voted!==-1?` · ${card.votes[i]} votes`:""}</button>`).join("")}</div></div></article>`).join("")||emptyHtml(t);$("feedCount").textContent=rateCards.length+" CARDS";return}
 if(view==="profile")list=posts.filter(p=>p.mine);
 if(view==="discover")list=[...posts].sort((a,b)=>b.likes-a.likes);
 $("feed").innerHTML=list.length?list.map(p=>`<article class="post card"><div class="posthead"><div class="avatar small">${safe(p.initial||initials(p.name))}</div><div class="grow"><div class="postname">${safe(p.name)}</div><div class="handle">${safe(p.handle||"@communitymember")}</div></div><span class="posttime">${safe(p.time||"now")}</span></div><div class="posttext">${safe(p.text)}</div>${p.tag?`<span class="tag">${safe(p.tag)}</span>`:""}<div class="actions"><button class="action ${p.liked?"liked":""}" data-like="${p.id}">♡ ${t.like} · ${p.likes}</button><button class="action" data-comment="${p.id}">◌ ${t.comment}</button><button class="action" data-share="${p.id}">↗ Share</button></div></article>`).join(""):emptyHtml(t);
 $("feedCount").textContent=list.length+" POSTS";
}
function emptyHtml(t){return `<div class="card empty"><strong>${t.empty}</strong>${t.emptyText}</div>`}
$("postBtn").onclick=()=>{let text=$("postInput").value.trim();if(!text){toast("Write something before sharing.");return}posts.unshift({id:Date.now(),name:name(),handle:"@"+name().toLowerCase().replace(/[^a-z0-9]+/g,""),initial:initials(name()),time:"now",text,likes:0,liked:false,mine:true,tag:"#MyRateMe"});$("postInput").value="";save();view="home";render();toast("Your post was added to this device!")}
$("displayName").oninput=()=>{$("myAvatar").textContent=initials(name())};
$("feed").addEventListener("click",e=>{
 let b=e.target.closest("button");if(!b)return;
 if(b.dataset.like){let p=posts.find(x=>x.id==b.dataset.like);if(p){p.liked=!p.liked;p.likes+=p.liked?1:-1;save();render()}}
 if(b.dataset.comment){let msg=prompt("Write a kind comment (demo only):");if(msg&&msg.trim())toast("Comment preview: "+msg.trim().slice(0,55)+" — comments will be saved when we connect the database.")}
 if(b.dataset.share){let p=posts.find(x=>x.id==b.dataset.share);if(p){let txt=p.text+" — on Rate Me";if(navigator.share)navigator.share({title:"Rate Me",text:txt}).catch(()=>{});else if(navigator.clipboard)navigator.clipboard.writeText(txt).then(()=>toast("Post text copied!"));else toast("Sharing is not available in this browser.")}}
 if(b.dataset.rate){let c=rateCards.find(x=>x.id==b.dataset.rate);if(c&&c.voted===-1){let i=Number(b.dataset.option);c.votes[i]++;c.voted=i;save();render();toast("Thanks for sharing your vote!")}}
});
function changeView(v){view=v;document.querySelectorAll("[data-view]").forEach(x=>x.classList.toggle("active",x.dataset.view===v));render();if(v==="profile")toast("Your posts on this device")}
document.querySelectorAll("[data-view]").forEach(x=>x.onclick=()=>changeView(x.dataset.view));
$("profileBtn").onclick=()=>changeView("profile");
document.querySelectorAll(".follow").forEach(b=>b.onclick=()=>{b.textContent=b.textContent==="Follow"?"Following":"Follow";toast("Demo follow updated")});
$("language").onchange=e=>setLanguage(e.target.value);
$("cancelModal").onclick=()=>$("modalBack").style.display="none";
$("createRate").onclick=()=>{let q=$("rateQuestion").value.trim(),opts=[$("rateOption1").value.trim(),$("rateOption2").value.trim(),$("rateOption3").value.trim()];if(!q||opts.some(x=>!x)){toast("Please complete the question and all options.");return}rateCards.unshift({id:Date.now(),name:name(),question:q,options:opts,votes:[0,0,0],voted:-1});save();$("modalBack").style.display="none";$("rateQuestion").value="";changeView("ratings");toast("Your rate card was created on this device!")};
document.addEventListener("keydown",e=>{if(e.key==="Escape")$("modalBack").style.display="none"});
// Add a create-card shortcut from the Rate tab's heading.
const rateShortcut=document.createElement("button");rateShortcut.className="btn soft";rateShortcut.textContent="＋ Create rate card";rateShortcut.onclick=()=>$("modalBack").style.display="flex";$("feedTitle").parentElement.appendChild(rateShortcut);
render();
</script>
</body>
</html>