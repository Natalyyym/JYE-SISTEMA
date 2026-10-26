[JE_Sistema_Administrativo_Actualizado (1).html](https://github.com/user-attachments/files/33976110/JE_Sistema_Administrativo_Actualizado.1.html)

<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>J&E | Sistema Administrativo</title>
<style>
:root {
  --navy:#10243a; --blue:#193b59; --yellow:#f5c542;
  --bg:#f3f6fa; --white:#fff; --text:#263445;
  --muted:#778497; --border:#e4eaf1; --red:#b42318;
}
*{box-sizing:border-box}
body{margin:0;font-family:Arial,sans-serif;background:var(--bg);color:var(--text)}
button,input,select{font:inherit}
button{cursor:pointer;border:0;border-radius:8px;padding:10px 13px;font-size:13px;font-weight:600}
.app{display:flex;min-height:100vh}
.sidebar{width:240px;background:var(--navy);color:white;padding:20px 13px;flex-shrink:0}
.brand{display:flex;align-items:center;gap:11px;padding:5px 8px 22px;border-bottom:1px solid #ffffff22}
.logo{background:var(--yellow);color:var(--navy);padding:12px;border-radius:10px;font-weight:900;font-size:22px}
.brand h2{font-size:18px;margin:0 0 5px}.brand small{color:#b9c8d7;font-size:11px}
.menu-label{font-size:10px;letter-spacing:1.5px;color:#94a8bc;margin:23px 10px 9px}
.nav{display:block;width:100%;text-align:left;background:transparent;color:#dce5ed;margin:3px 0;padding:12px 10px;font-weight:400}
.nav:hover,.nav.active{background:var(--blue);color:white}
.nav.active{border-left:4px solid var(--yellow)}
.main{flex:1;min-width:0}
.topbar{background:white;border-bottom:1px solid var(--border);padding:17px 25px;display:flex;align-items:center;justify-content:space-between;gap:12px}
.topbar h2{font-size:20px;margin:0 0 5px}.topbar small{color:var(--muted)}
.status{font-size:11px;color:#765b00;background:#fff4ce;padding:8px 10px;border-radius:8px}
.content{max-width:1450px;padding:24px;margin:auto}
.welcome{background:linear-gradient(120deg,var(--navy),var(--blue));color:white;padding:26px;border-radius:15px;margin-bottom:20px}
.welcome h1{margin:0 0 8px;font-size:25px}.welcome p{margin:0;color:#d4e0eb}
.cards{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:14px;margin:18px 0}
.card,.panel{background:white;border:1px solid var(--border);border-radius:12px}
.card{padding:17px;min-width:0}.card .label{font-size:12px;color:var(--muted)}
.card .value{font-size:23px;font-weight:700;margin:11px 0;overflow-wrap:anywhere}
.card small{font-size:11px;color:var(--muted)}
.panel{padding:19px;margin-bottom:18px}
.panel-head{display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap;margin-bottom:16px}
.panel h3{font-size:16px;margin:0}
.section-title{font-size:20px;margin:0 0 6px}
.subtitle{font-size:13px;color:var(--muted);margin:0 0 18px}
.primary{background:var(--yellow);color:var(--navy)}
.secondary{background:#eaf0f6;color:var(--navy)}
.danger{background:#ffebeb;color:var(--red)}
.search{width:100%;padding:12px;border:1px solid #d9e1eb;border-radius:9px;margin-bottom:14px;background:white}
.search:focus,input:focus,select:focus{outline:2px solid #f5c542;outline-offset:1px}
.table-wrap{overflow-x:auto}
table{border-collapse:collapse;width:100%;font-size:12px}
th,td{padding:12px 9px;text-align:left;border-bottom:1px solid var(--border);white-space:normal}
th{color:var(--muted);background:#fafbfd;font-weight:600}
.empty{text-align:center;color:var(--muted);padding:25px}
.form-grid{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:14px}
.field{display:flex;flex-direction:column;gap:7px}
.field label{font-size:12px;font-weight:600}
.field input,.field select{width:100%;padding:11px;border:1px solid #d9e1eb;border-radius:8px;background:white}
.actions{display:flex;gap:9px;flex-wrap:wrap;margin-top:16px}
.notice{background:#fff8df;border:1px solid #f1df9c;padding:12px;border-radius:9px;font-size:12px;line-height:1.6;margin-bottom:16px}
.muted{color:var(--muted);font-size:12px}
@media(max-width:1000px){.sidebar{width:205px}.cards{grid-template-columns:repeat(2,minmax(0,1fr))}.content{padding:17px}}
@media(max-width:650px){
 .app{display:block}.sidebar{width:100%;padding:12px}
 .brand{padding-bottom:13px}.menu-label{margin:15px 8px 7px}
 .nav-list{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:3px}
 .nav{font-size:12px;padding:10px;margin:0}
 .topbar{padding:14px}.topbar h2{font-size:17px}.status{font-size:9px}
 .content{padding:12px}.cards{gap:8px}.card{padding:12px}.card .value{font-size:19px}
 .welcome{padding:20px}.welcome h1{font-size:21px}.panel{padding:13px}
 .form-grid{grid-template-columns:1fr}
}
</style>
</head>
<body>
<div class="app">
<aside class="sidebar">
  <div class="brand">
    <div class="logo">J&E</div>
    <div><h2>J&E Sistema</h2><small>Administración del negocio</small></div>
  </div>
  <div class="menu-label">MENÚ PRINCIPAL</div>
  <div class="nav-list">
    <button class="nav" data-page="movimientos">↔ Ingresos y egresos</button>
    <button class="nav" data-page="inventario">🛢 Aceite</button>
    <button class="nav" data-page="ordenes">⚙ Órdenes de trabajo</button>
    <button class="nav" data-page="recibos">▤ Recibos de pago</button>
    <button class="nav" data-page="tarifas">🔧 Tarifas de servicios mecánicos</button>
    <button class="nav" data-page="serviciosAceite">🛢 Servicios de aceite</button>
    <button class="nav" data-page="clientes">♙ Clientes</button>
    <button class="nav" data-page="contabilidad">▣ Contabilidad / Libro diario</button>
    <button class="nav" data-page="reportes">▥ Reportes de cierre</button>
  </div>
  <div class="menu-label">SERVICIOS</div>
  <div style="padding:8px 10px;color:#bdcbd9;font-size:12px;line-height:1.9">
    Mecánica general<br>Maquinaria y equipo<br>Grúas y transporte
  </div>
</aside>

<main class="main">
<header class="topbar">
  <div><h2 id="pageTitle">Ingresos y egresos</h2><small id="today"></small></div>
  <div style="display:flex;align-items:center;gap:8px;flex-wrap:wrap;justify-content:flex-end">
    <div class="status" id="syncStatus">● Sin iniciar sesión</div>
    <button class="secondary" id="loginBtn" type="button">Iniciar sesión</button>
    <button class="primary" id="signupBtn" type="button">Crear cuenta</button>
    <button class="secondary" id="logoutBtn" type="button" style="display:none">Cerrar sesión</button>
  </div>
</header>
<div class="content" id="content"></div>
</main>
</div>

<script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
<script>
"use strict";

const $ = s => document.querySelector(s);

// Conexión de J&E con Supabase
const SUPABASE_URL = "https://jbwzwhnbjjtecverekqj.supabase.co";
const SUPABASE_PUBLISHABLE_KEY = "sb_publishable_K7X7Dxad2KSQ5J7BTLIa4w_dLg0GZ0W";
const supabaseClient = window.supabase?.createClient(SUPABASE_URL, SUPABASE_PUBLISHABLE_KEY);
let currentUser = null;
let realtimeChannel = null;
const DATA_KEYS = ["movimientos", "productos", "clientes", "ordenes", "inventarioMovimientos", "recibos", "serviciosAceite", "tarifas"];
let applyingCloudData = false;

function setSyncStatus(message) {
  const el = $("#syncStatus");
  if (el) el.textContent = message;
}
function updateAuthButtons() {
  $("#loginBtn").style.display = currentUser ? "none" : "";
  $("#signupBtn").style.display = currentUser ? "none" : "";
  $("#logoutBtn").style.display = currentUser ? "" : "none";
  setSyncStatus(currentUser ? "● Sincronización activada" : "● Solo en este dispositivo");
}
async function uploadData(key, value) {
  if (!supabaseClient || !currentUser || applyingCloudData) return;
  const { error } = await supabaseClient.from("je_data").upsert({
    user_id: currentUser.id,
    data_key: key,
    data_value: value,
    updated_at: new Date().toISOString()
  }, { onConflict: "user_id,data_key" });
  if (error) {
    console.error("Error al sincronizar", error);
    setSyncStatus("⚠ Error al sincronizar");
  } else {
    setSyncStatus("✓ Datos sincronizados");
  }
}
async function syncFromCloud() {
  if (!supabaseClient || !currentUser) return;
  setSyncStatus("● Sincronizando...");
  const { data, error } = await supabaseClient.from("je_data")
    .select("data_key,data_value").eq("user_id", currentUser.id);
  if (error) {
    console.error(error);
    setSyncStatus("⚠ No se pudo leer la nube");
    alert("No se pudieron cargar los datos de Supabase. Revisa que hayas ejecutado el SQL y que la tabla je_data exista.");
    return;
  }
  const cloudMap = new Map((data || []).map(row => [row.data_key, row.data_value]));
  applyingCloudData = true;
  const missingKeys = [];
  for (const key of DATA_KEYS) {
    if (cloudMap.has(key)) {
      localStorage.setItem("je_" + key, JSON.stringify(cloudMap.get(key) || []));
    } else {
      let localValue = [];
      try { localValue = JSON.parse(localStorage.getItem("je_" + key) || "[]"); } catch(e) {}
      missingKeys.push({ key, value: Array.isArray(localValue) ? localValue : [] });
    }
  }
  applyingCloudData = false;
  for (const item of missingKeys) await uploadData(item.key, item.value);
  render();
  setSyncStatus("✓ Sincronización activada");
  if (realtimeChannel) await supabaseClient.removeChannel(realtimeChannel);
  realtimeChannel = supabaseClient.channel("je-data-" + currentUser.id)
    .on("postgres_changes", { event: "*", schema: "public", table: "je_data", filter: "user_id=eq." + currentUser.id }, async () => {
      // Recargar los cambios que lleguen desde otro dispositivo.
      const { data: latest, error: latestError } = await supabaseClient.from("je_data")
        .select("data_key,data_value").eq("user_id", currentUser.id);
      if (!latestError && currentUser) {
        applyingCloudData = true;
        for (const row of latest || []) {
          if (DATA_KEYS.includes(row.data_key)) localStorage.setItem("je_" + row.data_key, JSON.stringify(row.data_value || []));
        }
        applyingCloudData = false;
        render();
        setSyncStatus("✓ Datos actualizados");
      }
    }).subscribe();
}
async function signUp() {
  if (!supabaseClient) { alert("No se pudo cargar la conexión con Supabase. Revisa tu conexión a internet."); return; }
  const email = prompt("Escribe el correo que usarás para J&E:");
  if (!email) return;
  const password = prompt("Crea una contraseña de al menos 6 caracteres:");
  if (!password) return;
  if (password.length < 6) { alert("La contraseña debe tener al menos 6 caracteres."); return; }
  const { data, error } = await supabaseClient.auth.signUp({ email: email.trim(), password });
  if (error) { alert("No se pudo crear la cuenta: " + error.message); return; }
  if (data.session) {
    currentUser = data.user;
    updateAuthButtons();
    await syncFromCloud();
    alert("Cuenta creada y sesión iniciada.");
  } else {
    alert("Cuenta creada. Revisa tu correo para confirmar la cuenta y después pulsa Iniciar sesión.");
  }
}
async function signIn() {
  if (!supabaseClient) { alert("No se pudo cargar la conexión con Supabase. Revisa tu conexión a internet."); return; }
  const email = prompt("Escribe tu correo de J&E:");
  if (!email) return;
  const password = prompt("Escribe tu contraseña:");
  if (!password) return;
  const { data, error } = await supabaseClient.auth.signInWithPassword({ email: email.trim(), password });
  if (error) { alert("No se pudo iniciar sesión: " + error.message); return; }
  currentUser = data.user;
  updateAuthButtons();
  await syncFromCloud();
}
async function signOut() {
  if (!supabaseClient) return;
  const { error } = await supabaseClient.auth.signOut();
  if (error) { alert("No se pudo cerrar sesión: " + error.message); return; }
  currentUser = null;
  if (realtimeChannel) await supabaseClient.removeChannel(realtimeChannel);
  realtimeChannel = null;
  updateAuthButtons();
}
$("#loginBtn").addEventListener("click", signIn);
$("#signupBtn").addEventListener("click", signUp);
$("#logoutBtn").addEventListener("click", signOut);
if (supabaseClient) {
  supabaseClient.auth.getSession().then(async ({ data, error }) => {
    if (!error && data.session) {
      currentUser = data.session.user;
      updateAuthButtons();
      await syncFromCloud();
    } else updateAuthButtons();
  });
} else {
  setSyncStatus("⚠ Sin conexión con Supabase");
}
const money = n => "Q " + Number(n||0).toLocaleString("es-GT",{
  minimumFractionDigits:2,maximumFractionDigits:2
});
const read = key => {
  try {
    const value = JSON.parse(localStorage.getItem("je_"+key)||"[]");
    return Array.isArray(value) ? value : [];
  } catch(e) { return []; }
};
const save = (key,value) => {
  localStorage.setItem("je_"+key, JSON.stringify(value));
  if (DATA_KEYS.includes(key)) void uploadData(key, value);
};
const esc = value => String(value??"").replace(/[&<>"']/g,c=>({
  "&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"
}[c]));
const todayISO = () => {
  const d=new Date();
  return d.getFullYear()+"-"+String(d.getMonth()+1).padStart(2,"0")+"-"+String(d.getDate()).padStart(2,"0");
};
$("#today").textContent=new Date().toLocaleDateString("es-GT",{
  day:"numeric",month:"long",year:"numeric"
});


// Listados iniciales transcritos del PDF entregado por el usuario. Solo se cargan si la lista está vacía.
const CLIENTES_INICIALES = [
["JUAN VELAZQUES","58639495"],["EDGAR YEPO","30329476"],["GREGORIO CALDERAS","42925718"],["WALTER NESTOR","53598649"],["WILLIAM COY","50477409"],["LEONEL","50904223"],["CHEPE NANA","30424573"],["ANGEL","59063799"],["PILOTO","43655214"],["CANCHE ALBAÑIL","55939611"],["YOLI","55350438"],["JOEL NANA","49757045"],["JULIO VELA","30028933"],["JAYRON ZANTISO","57585478"],["GERSON ZANTISO","30095864"],["JULIO GONZALES","45863344"],["PANCHO DOCTOR","57070255"],["MARCO TULIO","54473341"],["ONEYDA","31204198"],["DON OSCAR","58146940"],["JORGE QUIROPRACTICO","45498209"],["ABEL RAMOS","45695813"],["OSCAR PELUDO","53077625"],["KEVIN","54414049"],["CASILDO","40506969"],["JOSE HERNANDEZ","54186751"],["ESVIN GONZALES","47152395"],["CANCHE AGROPECUARIA","45203957"],["LUIS","45003134"],["ORLANDO VIELMAN/papa","45003134"],["ORLANDO VIELMAN/hijo","42204068"],["AMILCAR FARFAN","51795742"],["CAMARONAZO","41710472"],["CARNICERO","33040699"],["DON BETO","54939212"],["RODOLFO IRUN","41637645"],["DON EDI","58949359"],["ENMER SANTIZO","52339721"],["FORD PARRAMOS VACAS","41257062"],["HENRI PORRAS","33903331"],["GERVER MINCHES","59926548"],["LUIS GOMES","32131475"],["DON SELVIN","31517199"],["LUCA","59033245"],["JESSI GARCIA","50330766"],["DON CESAR","48926944"],["ROMUALDO","34240120"],["ZAPATERO","54473341"],["CANTINERO ROCAEL","52889520"],["EL PROFE","42987406"],["TIENDA","30117512"],["LUIS SUI","49785855"],["JORGE ESTEVAN","57707318"],["EDWIN AJPOP","51182705"],["ECTOR LOPEZ","59794923"],["JUAN SUARES","40564383"],["GUADALUPE","41257114"],["JULIO GOMES","55474730"],["SERGIO","51460631"],["OTRO JAIRON","46640997"],["EMILIANO","54497927"],["JULIO GERRA","48545192"],["MARCIAL","40450252"],["MAX","58274091"],["MAYCON/FRUTA","32424637 / 35745151"]
].map(([nombre,telefono])=>({nombre,telefono,nit:"",direccion:""}));
const PRODUCTOS_INICIALES = [
["G5W","5W30 FULL","Galón",410,1],["G10W","10W30","Galón",285,3],["L10W","10W30 litro","Litro",85,0],["G15W","15W40","Galón",285,3],["G20W","20W50","Galón",300,11],["L20W","20W50 litro","Litro",85,0],["L15W","15W40 litro","Litro",85,3],["L5W","5W30 litro","Litro",100,0],["GTX","20W50","Galón",285,3],["G80W","80W90","Galón",225,1],["G85W","85W140","Galón",225,0],["L80W","80W90 litro","Litro",65,6],["MAXG","Maxlife G","Galón",325,2],["MAXL","Maxlife L","Litro",100,11],["AH","Aceite hidráulico","Cubeta",435,0],["AM15","Aceite motor 15W40","Cubeta",650,0],["PS","Power stil","Litro",55,10],["SL","Silicon","Unidad",35,15],["UNG","Universal grande","Unidad",60,5],["UNP","Universal pequeño","Unidad",27,14],["CARBU","Carbuclin","Unidad",35,3],["G3","Grasa #3","Unidad",35,7],["candela 5101 GRISS","5101 BKR5E-11","Unidad",85,12],["candela 4424 AMARILLO","4424 BPR5ES-11","Unidad",85,16],["candela 4435 honda","4435 honda","Unidad",120,0],["candela 7079 AM/PLAT","7090 BKR5EGP","Unidad",150,4],["tap 331","tap 331","Unidad",50,3],["tap 329","tap 329","Unidad",50,3],["tap 109","tap 109","Unidad",45,2],["tap 111","tap 111","Unidad",45,3],["AFLOJ","Afloja todo","Unidad",35,0],["REF","Refrigerante","Galón",35,4],["FRENO","Líquido de freno STI","Litro",27,4],["ACEITE 10489A/51355","10489A/51356","Aceite",45,13],["ACEITE 10460A","10460A","Aceite",45,6],["ACEITE 10358","AUTOX 10358","Aceite",60,2],["ACEITE 7572A","7572A","Aceite",45,33],["ACEITE 10466A/51364","10466A/51365","Aceite",45,14],["ACEITE 51356","51356","Aceite",45,1],["ACEITE 7570","7570/87145","Aceite",45,14],["ACEITE F4967","TECH 4967","Aceite",45,4],["ACEITE 51034","51034","Aceite",50,0],["ACEITE 10583","10583","Aceite",60,6],["ACEITE 2W200","AUTOX 2W200","Aceite",45,1],["ACEITE 51523","51523","Aceite",125,4],["ACEITE 7573","7573","Aceite",95,2],["ACITE 10455A","10455A","Aceite",55,2],["ACEITE PH3950","FRAM 3950","Aceite",45,2],["DICEL 10675A","10675A","Diésel",95,0],["DICEL 33128","33128","Diésel",95,0],["DICEL KLINFIL 4831","4831","Diésel",75,2],["DICEL 2E900","AUTOX 2E900","Diésel",75,1],["DICEL 33390","33390","Diésel",75,2],["DICEL 33358","33358","Diésel",95,0],["DICEL 33138","33138","Diésel",90,0]
].map(([codigo,nombre,presentacion,precio,cantidad])=>({codigo,nombre,presentacion,precio,cantidad,costo:0,proveedor:"",mesRegistro:todayISO().slice(0,7)}));
// Artículos adicionales del inventario (páginas 2 a 7 del listado). Precio 0 significa que el PDF no indica un precio confirmado.
const PRODUCTOS_ADICIONALES = [
["UNO20W","20W50","Galón",0,0],["UNO10W","10W30 Plus","Galón",0,0],["GABRO","Grasa abro","Unidad",0,0],["BOSKH","FR78X-N50","Unidad",0,8],["CARTUCHO GAS","Cartucho con gas","Unidad",0,0],
["ACEITE 31922","AUTOX 31922","Aceite",0,3],["ACEITE 57243","57243","Aceite",0,0],["ACEITE 57145","57145","Aceite",0,0],["ACEITE MILL3614","3614","Aceite",0,0],["ACEITE 51383","51383","Aceite",0,4],
["DICEL 51622","51622","Diésel",0,0],["DICEL 51383","51383","Diésel",165,0],["DICEL 10558A","10558A","Diésel",0,1],["DICEL 33397","33397","Diésel",0,2],["AUTOX 620563","620563","Diésel",0,0],["TAEKO GASOLINA","P4920","Gasolina",0,1],["DICEL 6K6B0","6K6B0","Diésel",0,0],["DICEL 64016","64016","Diésel",0,0],["DICEL 17220","17220","Diésel",0,0],["DICEL 33395","33395","Diésel grúa",0,2],
["AIRE 188657","188657","Aire",0,2],["AIRE 281131R100","281131R100","Aire",0,2],["AIRE 28113-2800","28113-2800","Aire",0,1],["AIRE WL 80013Z40","WL 80013Z40","Aire",0,1],["AIRE LF 503Z40","LF 503Z40","Aire",0,1],
["FOCOS P21W","Foquitos P21W","Unidad",0,2],["SIN SELLADAS","Selladas","Sinchos",2,5],["SIN ABIERTAS","Abiertas","Sinchos",2,4],
["AIRE WIX 49247","WIX 49247","Aire",0,2],["AIRE ZYC 11299","ZYC 11299","Aire",0,2],["AIRE FA 5910","FA 5910","Aire",0,6],["AIRE AUTOX 1780121050","AUTOX 1780121050","Aire",0,2],["AIRE 1780122020","1780122020","Aire",0,2],["AIRE 1780135020","1780135020","Aire",0,4],["AIRE FIL PLUS 1780121050","FIL PLUS 1780121050","Aire",0,1],["AIRE 1780121030","1780121030","Aire",0,2],["AIRE FA 5709","FA 5709","Aire",0,1],["AIRE 1780131120","1780131120","Aire",0,2],["AIRE 17220Y2A000","17220Y2A000","Aire",0,3],["AIRE 17220R1AA01","17220R1AA01","Aire",0,2],["AIRE OKB023603","OKB023603","Aire",0,2],["AIRE 281134F000","281134F000","Aire",0,2],["AIRE MD 620563","MD 620563","Aire",0,3],["AIRE LA 5007","LA 5007","Aire",0,2],["AIRE 17200PNA003","17200PNA003","Aire",0,1],["AIRE FA 7902","FA 7902","Aire",0,1],
["ACEITE PH8A","41010","Aceite",0,4],["ACEITE 220900","220900","Aceite",0,2],["ACEITE 01034","01034","Aceite",0,2],["ACEITE 33010","33010","Aceite",0,1],["ACEITE 3387A","3387A","Aceite",0,2],["ACEITE 2F000","2F000","Aceite",0,2],["ACEITE AUTOX 612-2X","AUTOX 612-2X","Aceite",0,2],["ACEITE 10505","10505","Aceite grúa",0,1],
["DICEL TECH 10235","10235","Diésel",0,2],["DICEL TECH 4886","4886","Diésel",0,2],["DICEL 2330","23300364010","Diésel",0,1],["DICEL 23007","23307-64010","Diésel",0,2],["TRANSMISIÓN 51622","51622","Transmisión grúa",0,1],["CAJA 1215000","1215000","Caja",0,2],["CAJA 121500","121500","Caja",0,2],["LUBRICANTE","Lubricante","Unidad",0,12]
].map(([codigo,nombre,presentacion,precio,cantidad])=>({codigo,nombre,presentacion,precio,cantidad,costo:0,proveedor:"",mesRegistro:todayISO().slice(0,7)}));

const TARIFAS_INICIALES = [
["Servicio menor con filtro y aceite",75],["Servicio menor filtro aceite y candelas",125],["Cambio de pastillas",100],["Graduación de frenos de picop",50],["Graduación de frenos de camioncito",135],["Cambio de borner de batería",30],["Cambio de clotch carro sencillo y greis",500],["Cambio de candelas",80],["Cambio de resortaje y bujes",200],["Cambio de coginete y bufas",200],["Servicio mayor",475],["Poner y quitar alternador",150],["Calibración de válvulas",150],["Conversión de caja",1500],["Cambio de empaque culata liviano",600],["Si está cobrado como RAV",950],["Revisión",75],["Cambio de muleta",150],["Cambio de bujes con prensa",100],["Overhol liviano y buces Don Juan",300],["Servicio caja automática",150],["Rectificación de volante en torno",150],["Cambio de clotch camión Izusu",1200],["Quitar y poner radiador",200],["Quitar y poner starter",200],["Cambio de bomba de gasolina sumergible",350],["Quitar y poner censor",100],["Limpieza de carburador",125],["Cambio de bomba hidráulica",200],["Limpieza de inyectores",200],["Scanner",150],["Graduación de clotch",50],["Cambio de clotch carro doble",850],["Cambio de bomba de agua con fuga de tiempo",350],["Cambio de bomba de agua sin fuga de tiempo",150],["Cambio de turbo en Grace y otros",400],["Cambio de bomba de freno auxiliar",100],["Cambio de cruces (1 unidad)",100],["Cambio de cruces (2 unidades)",150],["Cambio de faja de tiempo",350],["Cambio de cargadores de motor",250],["Reparación de caja greis y sencillo",1350],["Bujes y reparación de caja doble",1950],["Cambio y reparación de caja sencillo",1200],["Actualización de censores de ángulo con scanner",400],["Cambio de balancines de greis",150],["Cambio de punta de flecha",150],["Cambio de retenedor de eje de levas",350],["Cambio de bomba de clotch",100],["Limpieza de cuerpo de aceleración",150],["Engrasado de coginetes y revisión de frenos y aceite",250],["Cambio amortiguadores camionetas y sedán (c/u)",150],["Cambio amortiguadores de pickups delanteros (c/u)",75]
].map(([nombre,precio])=>({nombre,precio,descripcion:""}));
const SERVICIOS_ACEITE_INICIALES = [
["Kia Sportage","5W30 Full 1 galón + 1 litro",495,"WL 10489A",45,"WIX 57054 / AUTOX 10358",""],["Toyota Corolla","5W30 1 galón",395,"AUTOX 10358",45,"",""],["Volkswagen / Volwaje","20W50 1 galón",270,"WL 7570",45,"",""],["Mazda modelo 86 y 89","20W50 1 galón",302,"WL 51356",45,"AUTOX 3816",85],["Nissan Frontier Chepe","20W50 1 galón",302,"WIX 7570",45,"",""],["Mazda CX5","5W30 1 galón",395,"WIX 10466A",45,"5910",""],["Hyundai H100","15W40 1 galón / 2 litros",302,"WL 10583",45,"N 7334",130],["Mazda 3-23","20W50 1 galón",270,"WL 10466A",45,"",""],["Mazda CX5","5W30 1 galón",270,"WL 7572",45,"F201-21-500 / Maxlife", ""],["Nissan Z24","20W50 1 galón",270,"WIX 15601",45,"",""],["Toyota Tacoma V6 Cantinero","20W50 1 galón + 1 litro",340,"WL 7570",45,"17801",""],["Toyota Yaris 2007","5W30 Full 1 galón",395,"WL 7572A",45,"FIL PLUS 17801",40],["Mazda BT50 Jordan","15W40 1 galón + 1 litro",480,"WIX 10455A",45,"",""],["Nissan Harvari y doble","20W50 1 galón",270,"WL 7570",45,"",""],["Mazda 3 2014/3 Eduar","5W30 1 galón",395,"WL 10489A",45,"AUTOX 11259 / FZ01 Maxlife", ""],["Honda CRV","20W50 1 galón",395,"WL 10489A / 10466A",45,"003 Maxlife", ""],["Mitsubishi Lanser Macario","10W30 1 galón",395,"",45,"",""],["Toyota Tacoma 22R","20W50 1 galón",302,"WL 7570",45,"5709",60],["Nissan 1991","20W50 1 galón + 1 litro",340,"WIX 51034",60,"",""],["Toyota Runer","20W50 1 galón + 1 litro",340,"WIX 7570",45,"",""],["Toyota RAV Chepe","20W50 1 galón",302,"WIX 7570",45,"WIX 9576",75],["Toyota modelo 88","20W50 1 galón",302,"WIX 3614",45,"",""],["Toyota 22R Anibal","10W30 1 galón",302,"WIX 7570",45,"",""],["Mitsubishi Montero","20W50 1 galón + 1 litro",302,"WIX 10489A",45,"",""],["Toyota 2011 Macario","10W30 1 galón",302,"WIX 10460A",45,"31120", ""],["Hyundai Accent 2015","5W30 1 galón",395,"WIX 10489A",45,"",""],["Mazda 3","10W30 1 galón",302,"WIX 10489A",45,"11259", ""],["Hyundai Tucson Selvin","15W40",263,"WIX ELE 263112F000",45,"28113-2S00 / 31922-2E900", ""],["Chevrolet Zonic Estefano","10W30 1 galón / 2 litros",0,"HU 612/2X",0,"",""],["Hyundai Matrix","",0,"",0,"XDR 12225 / Maxlife",150],["Honda Civic","10W30 1 galón",0,"WIX 10489A",45,"",""],["Hyundai H100","15W40 7 litros",0,"WIX 10675A",0,"",""],["Chevrolet Spark","5W30 1 galón",0,"WIX 7572A",0,"",""]
].map(([vehiculo,aceite,precioAceite,filtroAceite,precioFiltroAceite,filtroExtra,precioExtra])=>({vehiculo,aceite,precioAceite,filtroAceite,precioFiltroAceite,filtroExtra,precioExtra,notas:""}));
function seedIfEmpty(key, value){ if(!localStorage.getItem("je_"+key) || JSON.parse(localStorage.getItem("je_"+key)||"[]").length===0) localStorage.setItem("je_"+key,JSON.stringify(value)); }
seedIfEmpty("clientes",CLIENTES_INICIALES); seedIfEmpty("productos",[...PRODUCTOS_INICIALES,...PRODUCTOS_ADICIONALES]); seedIfEmpty("tarifas",TARIFAS_INICIALES); seedIfEmpty("serviciosAceite",SERVICIOS_ACEITE_INICIALES);
// Agrega los artículos que faltaban en versiones anteriores sin borrar cantidades ni cambios del usuario.
{ const saved=read("productos"); const keys=new Set(saved.map(x=>String(x.codigo||x.nombre).toLowerCase())); let changed=false;
  for(const item of [...PRODUCTOS_INICIALES,...PRODUCTOS_ADICIONALES]){const k=String(item.codigo||item.nombre).toLowerCase();if(!keys.has(k)){saved.push(item);keys.add(k);changed=true;}}
  if(changed)localStorage.setItem("je_productos",JSON.stringify(saved));
}

let page="movimientos";

const titles={
  movimientos:"Ingresos y egresos",
  inventario:"Aceite",clientes:"Clientes",
  ordenes:"Órdenes de trabajo",contabilidad:"Contabilidad / Libro diario",recibos:"Recibos de pago",reportes:"Reportes de cierre"
};

function field(label,name,placeholder="",type="text",required=true){
  return `<div class="field"><label>${label}</label>
  <input name="${name}" type="${type}" placeholder="${placeholder}"
  ${type==="number"?'min="0" step="0.01"':""}
  ${required?"required":""}></div>`;
}
function selectField(label,name,options){
  return `<div class="field"><label>${label}</label><select name="${name}" required>
  ${options.map(x=>`<option value="${esc(x)}">${esc(x)}</option>`).join("")}
  </select></div>`;
}
function searchBox(id,placeholder){
  return `<input class="search" id="${id}" type="search" placeholder="${placeholder}" aria-label="${placeholder}">`;
}
function table(headers,rows){
  return `<div class="table-wrap"><table><thead><tr>
  ${headers.map(h=>`<th>${h}</th>`).join("")}</tr></thead><tbody>
  ${rows.length?rows.join(""):`<tr><td colspan="${headers.length}" class="empty">No hay registros todavía.</td></tr>`}
  </tbody></table></div>`;
}
function searchableRow(values,html){
  return `<tr data-search="${esc(values.join(" ").toLowerCase())}">${html}</tr>`;
}
function filterTable(inputId,tableId){
  const input=$("#"+inputId), tableEl=$("#"+tableId);
  if(!input||!tableEl)return;
  const query=input.value.trim().toLocaleLowerCase();
  tableEl.querySelectorAll("tbody tr[data-search]").forEach(row=>{
    row.hidden=!row.dataset.search.includes(query);
  });
}
function bindSearch(inputId,tableId){
  const input=$("#"+inputId);
  if(input)input.addEventListener("input",()=>filterTable(inputId,tableId));
}
function go(nextPage){
  page=nextPage;
  document.querySelectorAll(".nav").forEach(b=>
    b.classList.toggle("active",b.dataset.page===page)
  );
  $("#pageTitle").textContent=titles[page];
  render();
}
document.querySelectorAll(".nav").forEach(b=>
  b.addEventListener("click",()=>go(b.dataset.page))
);

function editItem(key,index){
  const items=read(key); const item=items[index]; if(!item)return;
  const updated={...item};
  for(const k of Object.keys(item)){
    const value=prompt("Editar "+k+" (deja igual si no deseas cambiarlo):",String(item[k]??""));
    if(value===null)return;
    if(["precio","costo","cantidad","precioAceite","precioFiltroAceite","precioExtra"].includes(k) && value.trim()!=="") updated[k]=Number(value); else updated[k]=value;
  }
  items[index]=updated; save(key,items); render();
}
function removeItem(key,index){
  const items=read(key);
  if(index<0||index>=items.length)return;
  if(!confirm("¿Seguro que deseas eliminar este registro?"))return;
  items.splice(index,1);
  save(key,items);
  render();
}
function exportCSV(key){
  const items=read(key);
  if(!items.length){alert("No hay registros para exportar.");return;}
  const cols=[...new Set(items.flatMap(x=>Object.keys(x)))];
  const csv=[cols.join(";"),...items.map(x=>cols.map(k=>
    '"'+String(x[k]??"").replace(/"/g,'""')+'"'
  ).join(";"))].join("\r\n");
  const blob=new Blob(["\ufeff"+csv],{type:"text/csv;charset=utf-8;"});
  const url=URL.createObjectURL(blob);
  const a=document.createElement("a");
  a.href=url;a.download="JE_"+key+".csv";a.click();
  setTimeout(()=>URL.revokeObjectURL(url),1000);
}

function printDocument(title,body){
  const w=window.open("","_blank","width=850,height=700");
  if(!w){alert("Permite las ventanas emergentes para imprimir el documento.");return;}
  w.document.write(`<!doctype html><html lang="es"><head><meta charset="utf-8"><title>${title}</title><style>body{font-family:Arial,sans-serif;color:#222;padding:28px}h1{font-size:22px}h2{font-size:17px}hr{border:0;border-top:1px solid #aaa;margin:18px 0}.line{margin:10px 0}.box{border:1px solid #aaa;padding:12px;margin:12px 0}.muted{color:#555;font-size:12px}table{width:100%;border-collapse:collapse}td,th{border:1px solid #bbb;padding:8px;text-align:left}@media print{button{display:none}}</style></head><body>${body}<p class="muted">J&E · Mecánica general, maquinaria, grúas y transporte</p><script>window.onload=()=>window.print()<\/script></body></html>`);
  w.document.close();
}
function printOrder(i){
  const x=read("ordenes")[i]; if(!x)return;
  printDocument("Orden de trabajo J&E",`<h1>J&E — ORDEN DE TRABAJO</h1><div class="line"><b>No. de orden:</b> ${i+1} &nbsp; <b>Fecha:</b> ${esc(x.fecha)}</div><hr><h2>Datos del cliente y vehículo</h2><div class="line"><b>Cliente:</b> ${esc(x.cliente)}</div><div class="line"><b>Teléfono:</b> ${esc(x.telefono||"-")}</div><div class="line"><b>Vehículo:</b> ${esc(x.vehiculo)} &nbsp; <b>Placa:</b> ${esc(x.placa||"-")}</div><div class="box"><b>Trabajo solicitado</b><p>${esc(x.trabajo)}</p></div><table><tr><th>Concepto</th><th>Monto</th></tr><tr><td>Mano de obra</td><td>${money(x.mano)}</td></tr><tr><td>Repuestos y materiales</td><td>${money(x.repuestos)}</td></tr><tr><th>Total</th><th>${money(x.total)}</th></tr></table><p>Observaciones: ______________________________________________</p><br><div style="display:flex;justify-content:space-between;margin-top:45px"><span>________________________<br>Firma del cliente</span><span>________________________<br>Firma J&E</span></div>`);
}
function printReceiptByIndex(i){const x=read("recibos")[i];if(x)printReceipt(x);}
function printReceipt(x){
  printDocument("Recibo de pago J&E",`<h1>J&E — RECIBO DE PAGO</h1><div class="line"><b>Recibo No.:</b> ${esc(x.numero)} &nbsp; <b>Fecha:</b> ${esc(x.fecha)}</div><hr><div class="line"><b>Recibimos de:</b> ${esc(x.cliente)}</div><div class="line"><b>Concepto:</b> ${esc(x.concepto)}</div><div class="line"><b>Tipo:</b> ${esc(x.tipo)}</div><div class="line"><b>Vehículo / orden:</b> ${esc(x.referencia||"-")}</div><div class="box"><h2>Monto recibido: ${money(x.monto)}</h2><p><b>Forma de pago:</b> ${esc(x.pago)}</p></div><p>Saldo pendiente (si corresponde): ${money(x.saldo||0)}</p><br><div style="display:flex;justify-content:space-between;margin-top:45px"><span>________________________<br>Firma de quien recibe</span><span>________________________<br>Firma del cliente</span></div>`);
}
function render(){
  const c=$("#content");
  const moves=read("movimientos");
  const products=read("productos");
  const clients=read("clientes");
  const orders=read("ordenes");

  const income=moves.filter(x=>x.tipo==="Ingreso").reduce((s,x)=>s+Number(x.monto||0),0);
  const expense=moves.filter(x=>x.tipo==="Egreso").reduce((s,x)=>s+Number(x.monto||0),0);

  if(page==="inicio"){
    const recent=moves.slice(-5).reverse();
    c.innerHTML=`
    <section class="welcome"><h1>¡Bienvenido a J&E!</h1>
    <p>Controla las operaciones de tu negocio desde un solo lugar.</p></section>
    <div class="cards">
      <div class="card"><div class="label">Ingresos registrados</div><div class="value">${money(income)}</div><small>Movimientos de ingreso</small></div>
      <div class="card"><div class="label">Egresos registrados</div><div class="value">${money(expense)}</div><small>Movimientos de egreso</small></div>
      <div class="card"><div class="label">Diferencia registrada</div><div class="value">${money(income-expense)}</div><small>Ingresos menos egresos</small></div>
      <div class="card"><div class="label">Productos</div><div class="value">${products.length}</div><small>${clients.length} clientes · ${orders.length} órdenes</small></div>
    </div>
    <section class="panel">
      <div class="panel-head"><h3>Movimientos recientes</h3><button class="primary" id="newMove">+ Registrar movimiento</button></div>
      ${table(["Fecha","Tipo","Descripción","Monto"],recent.map(x=>searchableRow(
        [x.fecha,x.tipo,x.descripcion],
        `<td>${esc(x.fecha)}</td><td>${esc(x.tipo)}</td><td>${esc(x.descripcion)}</td><td>${money(x.monto)}</td>`
      )))}
    </section>
    <div class="notice">Inicia sesión con la misma cuenta de J&E en tu computadora y celular para sincronizar los datos. Si no has iniciado sesión, la información se guarda solo en este dispositivo.</div>`;
    $("#newMove").onclick=()=>go("movimientos");
  }

  if(page==="movimientos"){
    c.innerHTML=`
    <h3 class="section-title">Ingresos y egresos</h3>
    <p class="subtitle">Registra ventas, servicios, compras y gastos.</p>
    <section class="panel"><form id="moveForm">
      <div class="form-grid">
        ${selectField("Tipo de movimiento","tipo",["Ingreso","Egreso"])}
        ${selectField("Categoría","categoria",[
          "Venta de aceite","Venta de repuestos","Servicio de taller",
          "Servicio de grúa","Transporte","Compra de inventario",
          "Pago a trabajadores","Combustible","Mantenimiento",
          "Reparaciones","Servicios básicos","Papelería","Publicidad",
          "Gastos bancarios","Otros"
        ])}
        ${field("Descripción","descripcion","Ej. Cambio de aceite")}
        ${field("Monto en quetzales","monto","0.00","number")}
        ${field("Fecha","fecha","","date")}
        ${selectField("Forma de pago","pago",["Efectivo","Transferencia","Tarjeta","Crédito","Otro"])}
      </div>
      <div class="actions"><button class="primary">Guardar movimiento</button><button class="secondary" type="reset">Limpiar</button></div>
    </form></section>
    <section class="panel">
      <div class="panel-head"><h3>Historial</h3><button class="secondary" id="exportMoves">Exportar CSV</button></div>
      ${searchBox("searchMoves","Buscar por fecha, tipo, categoría o descripción...")}
      ${table(["Fecha","Tipo","Categoría","Descripción","Monto","Acción"],
      moves.map((x,i)=>searchableRow(
        [x.fecha,x.tipo,x.categoria,x.descripcion,x.pago],
        `<td>${esc(x.fecha)}</td><td>${esc(x.tipo)}</td><td>${esc(x.categoria)}</td><td>${esc(x.descripcion)}</td><td>${money(x.monto)}</td><td><button class="secondary" onclick="editItem('movimientos',${i})">Editar</button> <button class="danger" onclick="removeItem('movimientos',${i})">Eliminar</button></td>`
      )))}
    </section>`;
    $("#moveForm").fecha.value=todayISO();
    $("#moveForm").addEventListener("submit",e=>{
      e.preventDefault();
      const d=Object.fromEntries(new FormData(e.target));
      d.monto=Number(d.monto);
      if(!Number.isFinite(d.monto)||d.monto<=0){alert("Ingresa un monto mayor que cero.");return;}
      moves.push(d);save("movimientos",moves);render();
    });
    bindSearch("searchMoves","content table");
    $("#exportMoves").onclick=()=>exportCSV("movimientos");
  }

  if(page==="inventario"){
    const invMoves=read("inventarioMovimientos");
    c.innerHTML=`
    <h3 class="section-title">Aceite y repuestos</h3>
    <p class="subtitle">Registra productos, cantidades, costos y precios de venta.</p>
    <section class="panel"><form id="productForm">
      <div class="form-grid">
        ${field("Código del producto","codigo","Ej. G5W","text",false)}
        ${field("Nombre del producto","nombre","Ej. Aceite 15W-40")}
        ${field("Presentación","presentacion","Galón, litro, unidad...","text",false)}
        ${field("Cantidad inicial del mes","cantidad","0","number")}
        ${field("Costo de compra por unidad (Q)","costo","0.00","number")}
        ${field("Proveedor","proveedor","Nombre del proveedor")}
        ${field("Precio de venta por unidad (Q)","precio","0.00","number")}
        <div class="field"><label>Ganancia por unidad</label><input id="gananciaPreview" value="Q 0.00" readonly></div>
      </div>
      <div class="actions"><button class="primary">Agregar producto</button></div>
    </form></section>
    <section class="panel"><h3>Registrar entrada o salida de producto</h3>
      <p class="subtitle">Las entradas aumentan las existencias y las salidas las disminuyen.</p>
      <form id="stockForm"><div class="form-grid">
        ${selectField("Tipo de movimiento","tipo",["Entrada","Salida"])}
        <div class="field"><label>Producto</label><select name="producto" required>${products.map((x,i)=>`<option value="${i}">${esc(x.nombre)} — existencias: ${Number(x.cantidad)}</option>`).join("")}</select></div>
        ${field("Cantidad","cantidad","0","number")}
        ${field("Fecha","fecha","","date")}
        ${field("Carro / vehículo donde se usa","vehiculo","Ej. Toyota Corolla, placa...", "text",false)}
        ${field("Número de orden de trabajo","orden","Ej. OT-025", "text",false)}
        ${field("Motivo / descripción","descripcion","Ej. Compra de aceite o uso en reparación")}
      </div><div class="actions"><button class="primary">Guardar movimiento de aceite</button></div></form>
    </section>
    <section class="panel"><div class="panel-head"><h3>Historial de entradas y salidas</h3><button class="secondary" id="exportStock">Exportar CSV</button></div>
      ${table(["Fecha","Tipo","Producto","Cantidad","Carro / vehículo","Orden","Descripción"],invMoves.slice().reverse().map(x=>searchableRow([x.fecha,x.tipo,x.producto,x.vehiculo,x.orden,x.descripcion],`<td>${esc(x.fecha)}</td><td>${esc(x.tipo)}</td><td>${esc(x.producto)}</td><td>${Number(x.cantidad)}</td><td>${esc(x.vehiculo||"-")}</td><td>${esc(x.orden||"-")}</td><td>${esc(x.descripcion)}</td>`)))}
    </section>
    <section class="panel">
      <div class="panel-head"><h3>Productos registrados en Aceite</h3><button class="secondary" id="exportProducts">Exportar CSV</button></div>
      ${searchBox("searchProducts","Buscar por nombre o código de producto...")}
      ${table(["Producto","Existencia","Proveedor","Costo de compra","Precio de venta","Ganancia por unidad","Ganancia potencial","Acción"],
      products.map((x,i)=>searchableRow(
        [x.codigo,x.nombre,x.proveedor],
        `<td>${esc((x.codigo?x.codigo+" — ":"")+x.nombre)}</td><td>${Number(x.cantidad)||0}</td><td>${esc(x.proveedor||"-")}</td><td>${money(x.costo)}</td><td>${money(x.precio)}</td><td>${money(Number(x.precio||0)-Number(x.costo||0))}</td><td>${money((Number(x.precio||0)-Number(x.costo||0))*Number(x.cantidad||0))}</td><td><button class="secondary" onclick="editItem('productos',${i})">Editar</button> <button class="danger" onclick="removeItem('productos',${i})">Eliminar</button></td>`
      )))}
    </section>`;
    $("#productForm").addEventListener("submit",e=>{
      e.preventDefault();
      const d=Object.fromEntries(new FormData(e.target));
      for(const k of ["cantidad","costo","precio"])d[k]=Number(d[k]||0);
      if(d.cantidad<0||d.costo<0||d.precio<0){alert("Las cantidades y los precios no pueden ser negativos.");return;}
      d.gananciaUnidad=d.precio-d.costo;
      d.mesRegistro=todayISO().slice(0,7);
      products.push(d);save("productos",products);render();
    });
    const costInput=$("#productForm [name=costo]"), priceInput=$("#productForm [name=precio]"), gainPreview=$("#gananciaPreview");
    const updateGain=()=>{if(gainPreview)gainPreview.value=money(Number(priceInput.value||0)-Number(costInput.value||0));};
    costInput.addEventListener("input",updateGain); priceInput.addEventListener("input",updateGain);
    bindSearch("searchProducts","content table");
    $("#exportProducts").onclick=()=>exportCSV("productos");
    if(products.length){ $("#stockForm").fecha.value=todayISO(); }
    $("#stockForm").addEventListener("submit",e=>{
      e.preventDefault(); const d=Object.fromEntries(new FormData(e.target));
      d.cantidad=Number(d.cantidad); const idx=Number(d.producto); const product=products[idx];
      if(!product){alert("Primero agrega un producto al inventario.");return;}
      if(!Number.isFinite(d.cantidad)||d.cantidad<=0){alert("Ingresa una cantidad mayor que cero.");return;}
      if(d.tipo==="Salida"&&d.cantidad>Number(product.cantidad)){alert("No hay suficiente existencia para registrar esa salida.");return;}
      product.cantidad=Number(product.cantidad)+(d.tipo==="Entrada"?d.cantidad:-d.cantidad);
      d.productoNombre=product.nombre; invMoves.push({fecha:d.fecha,tipo:d.tipo,producto:product.nombre,cantidad:d.cantidad,vehiculo:d.vehiculo||"",orden:d.orden||"",descripcion:d.descripcion});
      save("productos",products);save("inventarioMovimientos",invMoves);render();
    });
    const stockExport=$("#exportStock"); if(stockExport)stockExport.onclick=()=>exportCSV("inventarioMovimientos");
  }

  if(page==="clientes"){
    c.innerHTML=`
    <h3 class="section-title">Clientes</h3><p class="subtitle">Guarda la información de contacto de tus clientes.</p>
    <section class="panel"><form id="clientForm">
      <div class="form-grid">
        ${field("Nombre completo","nombre","Nombre del cliente")}
        ${field("Teléfono","telefono","Número de contacto","tel")}
        ${field("NIT","nit","NIT (opcional)","text",false)}
        ${field("Dirección","direccion","Dirección (opcional)","text",false)}
      </div><div class="actions"><button class="primary">Guardar cliente</button></div>
    </form></section>
    <section class="panel"><div class="panel-head"><h3>Clientes registrados</h3><button class="secondary" id="exportClients">Exportar CSV</button></div>
      ${searchBox("searchClients","Buscar por nombre, teléfono, NIT o dirección...")}
      ${table(["Nombre","Teléfono","NIT","Dirección","Acción"],clients.map((x,i)=>searchableRow(
        [x.nombre,x.telefono,x.nit,x.direccion],
        `<td>${esc(x.nombre)}</td><td>${esc(x.telefono)}</td><td>${esc(x.nit||"-")}</td><td>${esc(x.direccion||"-")}</td><td><button class="secondary" onclick="editItem('clientes',${i})">Editar</button> <button class="danger" onclick="removeItem('clientes',${i})">Eliminar</button></td>`
      )))}
    </section>`;
    $("#clientForm").addEventListener("submit",e=>{
      e.preventDefault();
      clients.push(Object.fromEntries(new FormData(e.target)));
      save("clientes",clients);render();
    });
    bindSearch("searchClients","content table");
    $("#exportClients").onclick=()=>exportCSV("clientes");
  }

  if(page==="ordenes"){
    c.innerHTML=`
    <h3 class="section-title">Órdenes de trabajo</h3><p class="subtitle">Controla vehículos, reparaciones y cobros.</p>
    <section class="panel"><form id="orderForm">
      <div class="form-grid">
        ${field("Fecha","fecha","","date")}
        <div class="field"><label>Cliente registrado (opcional)</label>
          <select name="clienteId"><option value="">Seleccionar cliente...</option>
          ${clients.map((x,i)=>`<option value="${i}">${esc(x.nombre)}</option>`).join("")}
          </select>
        </div>
        ${field("Nombre del cliente","cliente","Nombre del cliente")}
        ${field("Teléfono","telefono","Número de contacto","tel",false)}
        ${field("Vehículo / marca","vehiculo","Ej. Toyota Hilux")}
        ${field("Placa","placa","Número de placa","text",false)}
        ${field("Trabajo solicitado","trabajo","Descripción del servicio")}
        ${field("Mano de obra (Q)","mano","0.00","number")}
        ${field("Repuestos y materiales (Q)","repuestos","0.00","number")}
        ${field("Total cobrado (Q)","total","0.00","number")}
      </div><div class="actions"><button class="primary">Guardar orden</button></div>
    </form></section>
    <section class="panel">
      <div class="panel-head"><h3>Órdenes registradas</h3><button class="secondary" id="exportOrders">Exportar CSV</button></div>
      ${searchBox("searchOrders","Buscar por cliente, teléfono, vehículo, placa o trabajo...")}
      ${table(["Fecha","Cliente","Teléfono","Vehículo","Placa","Trabajo","Total","Acción"],
      orders.map((x,i)=>searchableRow(
        [x.fecha,x.cliente,x.telefono,x.vehiculo,x.placa,x.trabajo],
        `<td>${esc(x.fecha)}</td><td>${esc(x.cliente)}</td><td>${esc(x.telefono||"-")}</td><td>${esc(x.vehiculo)}</td><td>${esc(x.placa||"-")}</td><td>${esc(x.trabajo)}</td><td>${money(x.total)}</td><td><button class="secondary" onclick="printOrder(${i})">Imprimir</button> <button class="secondary" onclick="editItem('ordenes',${i})">Editar</button> <button class="danger" onclick="removeItem('ordenes',${i})">Eliminar</button></td>`
      )))}
    </section>`;
    $("#orderForm").fecha.value=todayISO();
    $("#orderForm").clienteId.addEventListener("change",e=>{
      const i=e.target.value;
      if(i!==""&&clients[i]){
        $("#orderForm").cliente.value=clients[i].nombre;
        $("#orderForm").telefono.value=clients[i].telefono||"";
      }
    });
    $("#orderForm").addEventListener("submit",e=>{
      e.preventDefault();
      const d=Object.fromEntries(new FormData(e.target));
      for(const k of ["mano","repuestos","total"])d[k]=Number(d[k]||0);
      if(!Number.isFinite(d.total)||d.total<0){alert("Revisa el total de la orden.");return;}
      orders.push(d);save("ordenes",orders);render();
    });
    bindSearch("searchOrders","content table");
    $("#exportOrders").onclick=()=>exportCSV("ordenes");
  }

  if(page==="contabilidad"){
    const stock=products.reduce((s,x)=>s+Number(x.cantidad)*Number(x.costo),0);
    c.innerHTML=`
    <h3 class="section-title">Resumen contable</h3><p class="subtitle">Vista general de los movimientos registrados.</p>
    <div class="cards">
      <div class="card"><div class="label">Ingresos registrados</div><div class="value">${money(income)}</div></div>
      <div class="card"><div class="label">Egresos registrados</div><div class="value">${money(expense)}</div></div>
      <div class="card"><div class="label">Inventario al costo</div><div class="value">${money(stock)}</div></div>
      <div class="card"><div class="label">Diferencia</div><div class="value">${money(income-expense)}</div></div>
    </div>
    <div class="notice"><b>Nota:</b> este módulo todavía no genera libros oficiales. Para elaborar el Libro Diario, Mayor, Balance de Comprobación y estados financieros se requiere configurar el catálogo de cuentas y generar partidas con debe y haber balanceados.</div>
    <section class="panel"><div class="panel-head"><h3>Libro diario de ingresos y egresos</h3><button class="secondary" onclick="go('movimientos')">Registrar movimiento</button></div>
      <div class="field"><label>Consultar fecha</label><input type="date" id="diarioFecha" value="${todayISO()}"></div><div id="diarioResultado"></div>
    </section>`;
    const drawDiary=()=>{const day=$("#diarioFecha").value;const list=moves.filter(x=>x.fecha===day);const ins=list.filter(x=>x.tipo==="Ingreso").reduce((a,x)=>a+Number(x.monto||0),0);const outs=list.filter(x=>x.tipo==="Egreso").reduce((a,x)=>a+Number(x.monto||0),0);$("#diarioResultado").innerHTML=`<div class="cards"><div class="card"><div class="label">Ingresos del día</div><div class="value">${money(ins)}</div></div><div class="card"><div class="label">Egresos del día</div><div class="value">${money(outs)}</div></div><div class="card"><div class="label">Diferencia</div><div class="value">${money(ins-outs)}</div></div></div>${table(["Fecha","Tipo","Categoría","Descripción","Forma de pago","Monto"],list.map(x=>`<tr><td>${esc(x.fecha)}</td><td>${esc(x.tipo)}</td><td>${esc(x.categoria)}</td><td>${esc(x.descripcion)}</td><td>${esc(x.pago)}</td><td>${money(x.monto)}</td></tr>`))}<div class="actions"><button class="secondary" id="printDiary">Imprimir libro diario del día</button></div>`;const b=$("#printDiary");b.onclick=()=>printDocument("Libro diario J&E",`<h1>J&E — LIBRO DIARIO</h1><p>Fecha: ${esc(day)}</p><p>Ingresos: ${money(ins)} &nbsp; Egresos: ${money(outs)} &nbsp; Diferencia: ${money(ins-outs)}</p>${table(["Fecha","Tipo","Categoría","Descripción","Forma de pago","Monto"],list.map(x=>`<tr><td>${esc(x.fecha)}</td><td>${esc(x.tipo)}</td><td>${esc(x.categoria)}</td><td>${esc(x.descripcion)}</td><td>${esc(x.pago)}</td><td>${money(x.monto)}</td></tr>`))}`);};
    $("#diarioFecha").addEventListener("change",drawDiary);drawDiary();
  }

  if(page==="recibos"){
    const receipts=read("recibos");
    const nextNo=String(receipts.length+1).padStart(5,"0");
    c.innerHTML=`<h3 class="section-title">Recibos de pago y adelantos</h3><p class="subtitle">Registra anticipos para repuestos, abonos y pagos de clientes. Puedes imprimir cada comprobante.</p>
    <section class="panel"><form id="receiptForm"><div class="form-grid">
      ${field("Número de recibo","numero",nextNo)}
      ${field("Fecha","fecha","","date")}
      ${field("Nombre del cliente","cliente","Nombre completo")}
      ${selectField("Tipo de recibo","tipo",["Adelanto para repuestos","Abono a cuenta","Pago de servicio","Pago total","Otro"])}
      ${field("Concepto / detalle","concepto","Ej. Adelanto para compra de repuestos")}
      ${field("Vehículo o número de orden (opcional)","referencia","Ej. Toyota Hilux / Orden 12","text",false)}
      ${field("Monto recibido (Q)","monto","0.00","number")}
      ${selectField("Forma de pago","pago",["Efectivo","Transferencia","Tarjeta","Cheque","Otro"])}
      ${field("Saldo pendiente (Q, si aplica)","saldo","0.00","number",false)}
    </div><div class="actions"><button class="primary">Guardar recibo</button></div></form></section>
    <section class="panel"><div class="panel-head"><h3>Recibos registrados</h3><button class="secondary" id="exportReceipts">Exportar CSV</button></div>${searchBox("searchReceipts","Buscar por número, cliente o concepto...")}${table(["No.","Fecha","Cliente","Tipo","Concepto","Monto","Acciones"],receipts.map((x,i)=>searchableRow([x.numero,x.fecha,x.cliente,x.tipo,x.concepto],`<td>${esc(x.numero)}</td><td>${esc(x.fecha)}</td><td>${esc(x.cliente)}</td><td>${esc(x.tipo)}</td><td>${esc(x.concepto)}</td><td>${money(x.monto)}</td><td><button class="secondary" onclick="printReceiptByIndex(${i})">Imprimir</button> <button class="secondary" onclick="editItem('recibos',${i})">Editar</button> <button class="danger" onclick="removeItem('recibos',${i})">Eliminar</button></td>`)))}</section>`;
    $("#receiptForm").fecha.value=todayISO();
    $("#receiptForm").addEventListener("submit",e=>{e.preventDefault();const d=Object.fromEntries(new FormData(e.target));d.monto=Number(d.monto||0);d.saldo=Number(d.saldo||0);if(d.monto<=0){alert("Ingresa un monto recibido mayor que cero.");return;}receipts.push(d);save("recibos",receipts);render();});
    bindSearch("searchReceipts","content table");$("#exportReceipts").onclick=()=>exportCSV("recibos");
  }

  if(page==="serviciosAceite"){
    const list=read("serviciosAceite");
    c.innerHTML=`<h3 class="section-title">Servicios de aceite</h3><p class="subtitle">Busca por vehículo, tipo de aceite o filtro. Los precios en cero o vacíos deben confirmarse antes de cobrar.</p>
    <section class="panel"><form id="oilServiceForm"><div class="form-grid">
      ${field("Vehículo / cliente","vehiculo","Ej. Toyota Corolla")}${field("Aceite y cantidad","aceite","Ej. 20W50, 1 galón")}${field("Precio del aceite (Q)","precioAceite","0","number",false)}${field("Filtro de aceite","filtroAceite","Código de filtro", "text",false)}${field("Precio filtro aceite (Q)","precioFiltroAceite","0","number",false)}${field("Filtro adicional / aire / diésel","filtroExtra","Código", "text",false)}${field("Precio filtro adicional (Q)","precioExtra","0","number",false)}${field("Notas","notas","Observaciones", "text",false)}
    </div><div class="actions"><button class="primary">Agregar servicio de aceite</button></div></form></section>
    <section class="panel"><div class="panel-head"><h3>Listado de servicios</h3><button class="secondary" id="exportOil">Exportar CSV</button></div>${searchBox("searchOil","Buscar vehículo, aceite o filtro...")}${table(["Vehículo","Aceite","Precio aceite","Filtro aceite","Precio filtro","Filtro adicional","Precio adicional","Acciones"],list.map((x,i)=>searchableRow(Object.values(x),`<td>${esc(x.vehiculo)}</td><td>${esc(x.aceite||"-")}</td><td>${x.precioAceite?money(x.precioAceite):"Por confirmar"}</td><td>${esc(x.filtroAceite||"-")}</td><td>${x.precioFiltroAceite?money(x.precioFiltroAceite):"Por confirmar"}</td><td>${esc(x.filtroExtra||"-")}</td><td>${x.precioExtra?money(x.precioExtra):"Por confirmar"}</td><td><button class="secondary" onclick="editItem('serviciosAceite',${i})">Editar</button> <button class="danger" onclick="removeItem('serviciosAceite',${i})">Eliminar</button></td>`)))}</section>`;
    $("#oilServiceForm").addEventListener("submit",e=>{e.preventDefault();const d=Object.fromEntries(new FormData(e.target));for(const k of ["precioAceite","precioFiltroAceite","precioExtra"])d[k]=Number(d[k]||0);list.push(d);save("serviciosAceite",list);render();});bindSearch("searchOil","content table");$("#exportOil").onclick=()=>exportCSV("serviciosAceite");
  }
  if(page==="tarifas"){
    const list=read("tarifas");
    c.innerHTML=`<h3 class="section-title">Tarifas de servicios mecánicos</h3><p class="subtitle">Lista de referencia para consultar cuánto se cobra por cada trabajo. Puedes modificar las tarifas cuando sea necesario.</p>
    <section class="panel"><form id="tariffForm"><div class="form-grid">${field("Nombre del trabajo","nombre","Ej. Cambio de pastillas")}${field("Precio (Q)","precio","0.00","number")}${field("Descripción o condición (opcional)","descripcion","Ej. precio por unidad", "text",false)}</div><div class="actions"><button class="primary">Agregar tarifa</button></div></form></section>
    <section class="panel"><div class="panel-head"><h3>Tarifas registradas</h3><button class="secondary" id="exportTariffs">Exportar CSV</button><button class="secondary" onclick="printDocument('Tarifas de servicios mecánicos', '<h1>J&E — TARIFAS DE TRABAJOS MECÁNICOS</h1>'+document.querySelector('#tariffTable').outerHTML)">Imprimir tarifas</button></div>${searchBox("searchTariffs","Buscar trabajo mecánico...")}<div id="tariffTable">${table(["Trabajo","Precio","Descripción","Acciones"],list.map((x,i)=>searchableRow([x.nombre,x.descripcion],`<td>${esc(x.nombre)}</td><td>${money(x.precio)}</td><td>${esc(x.descripcion||"-")}</td><td><button class="secondary" onclick="editItem('tarifas',${i})">Editar</button> <button class="danger" onclick="removeItem('tarifas',${i})">Eliminar</button></td>`)))}</div></section>`;
    $("#tariffForm").addEventListener("submit",e=>{e.preventDefault();const d=Object.fromEntries(new FormData(e.target));d.precio=Number(d.precio||0);list.push(d);save("tarifas",list);render();});bindSearch("searchTariffs","content table");$("#exportTariffs").onclick=()=>exportCSV("tarifas");
  }

  if(page==="reportes"){
    const mesActual=todayISO().slice(0,7);
    c.innerHTML=`
    <h3 class="section-title">Reportes semanales y mensuales</h3>
    <p class="subtitle">Selecciona cualquier mes para consultar sus resultados.</p>
    <section class="panel">
      <div class="field"><label>Mes del reporte</label><input type="month" id="mesReporte" value="${mesActual}"></div>
      <div class="actions"><button class="primary" id="exportReport">Exportar movimientos del mes</button></div>
    </section>
    <div id="resultadoReporte"></div>`;
    const calculate=mes=>{
      if(!/^\d{4}-\d{2}$/.test(mes||""))return "<p>Selecciona un mes válido.</p>";
      const [year,month]=mes.split("-").map(Number);
      const lastDay=new Date(year,month,0).getDate();
      const list=moves.filter(m=>m.fecha&&m.fecha.startsWith(mes)&&
        /^\d{4}-\d{2}-\d{2}$/.test(m.fecha));
      const sum=a=>a.reduce((s,m)=>s+Number(m.monto||0),0);
      const inTotal=sum(list.filter(m=>m.tipo==="Ingreso"));
      const outTotal=sum(list.filter(m=>m.tipo==="Egreso"));
      const iso=d=>year+"-"+String(month).padStart(2,"0")+"-"+String(d).padStart(2,"0");
      const fmt=d=>new Date(year,month-1,d).toLocaleDateString("es-GT",{day:"2-digit",month:"2-digit"});
      let weeks=[];
      // Semana 1 empieza el día 1 y termina el primer domingo.
      // Las siguientes van de lunes a domingo, hasta el final del mes.
      let start=1;
      while(start<=lastDay){
        let end=Math.min(lastDay,start+(start===1?((7-new Date(year,month-1,start).getDay())%7):6));
        const week=list.filter(m=>m.fecha>=iso(start)&&m.fecha<=iso(end));
        const ins=sum(week.filter(m=>m.tipo==="Ingreso"));
        const outs=sum(week.filter(m=>m.tipo==="Egreso"));
        weeks.push({start,end,ins,outs,count:week.length});
        start=end+1;
      }
      return `
      <div class="cards">
        <div class="card"><div class="label">Ingresos del mes</div><div class="value">${money(inTotal)}</div></div>
        <div class="card"><div class="label">Egresos del mes</div><div class="value">${money(outTotal)}</div></div>
        <div class="card"><div class="label">Diferencia mensual</div><div class="value">${money(inTotal-outTotal)}</div></div>
        <div class="card"><div class="label">Movimientos</div><div class="value">${list.length}</div></div>
      </div>
      <section class="panel"><div class="panel-head"><h3>Detalle semanal</h3></div>
        ${table(["Semana","Fechas","Ingresos","Egresos","Diferencia","Movimientos"],
          weeks.map((w,i)=>`<tr><td>Semana ${i+1}</td><td>${fmt(w.start)} - ${fmt(w.end)}</td><td>${money(w.ins)}</td><td>${money(w.outs)}</td><td>${money(w.ins-w.outs)}</td><td>${w.count}</td></tr>`)
          .concat([`<tr><td colspan="2"><b>TOTAL MENSUAL</b></td><td><b>${money(inTotal)}</b></td><td><b>${money(outTotal)}</b></td><td><b>${money(inTotal-outTotal)}</b></td><td><b>${list.length}</b></td></tr>`]))}
      </section>
      <div class="notice">Los movimientos se agrupan por fecha. La primera semana empieza el día 1 del mes y termina el primer domingo; las siguientes se cuentan de lunes a domingo. La diferencia no equivale necesariamente a la utilidad contable.</div>`;
    };
    const update=()=>$("#resultadoReporte").innerHTML=calculate($("#mesReporte").value);
    $("#mesReporte").addEventListener("change",update);
    $("#exportReport").onclick=()=>{
      const mes=$("#mesReporte").value;
      const list=read("movimientos").filter(m=>m.fecha&&m.fecha.startsWith(mes));
      if(!list.length){alert("No hay movimientos para este mes.");return;}
      const cols=["fecha","tipo","categoria","descripcion","monto","pago"];
      const csv=[cols.join(";"),...list.map(m=>cols.map(k=>
        '"'+String(m[k]??"").replace(/"/g,'""')+'"'
      ).join(";"))].join("\r\n");
      const blob=new Blob(["\ufeff"+csv],{type:"text/csv;charset=utf-8;"});
      const url=URL.createObjectURL(blob);
      const a=document.createElement("a");
      a.href=url;a.download="JE_Reporte_"+mes+".csv";a.click();
      setTimeout(()=>URL.revokeObjectURL(url),1000);
    };
    update();
  }
}
render();
</script>
</body>
</html>
