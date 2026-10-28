<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#080d14">
<title>MAX VPN MOZ</title>
<style>
:root{--green:#00e68a;--bg:#080d14;--panel:#111b28;--muted:#9aabba}
*{box-sizing:border-box}
body{margin:0;background:radial-gradient(ellipse at top,#123326 0%,var(--bg) 48%);color:white;font-family:Arial,sans-serif;min-height:100vh}
header{max-width:900px;margin:auto;padding:24px 20px;display:flex;align-items:center;gap:12px}
.logo{height:48px;width:48px;border-radius:15px;background:var(--green);color:#06130d;display:grid;place-items:center;font-size:26px;font-weight:bold}
.brand{font-size:19px;font-weight:900;color:var(--green)}
.sub{font-size:10px;letter-spacing:2px;color:var(--muted);margin-top:5px}
main{max-width:560px;margin:30px auto;padding:20px}
.card{background:rgba(17,27,40,.94);border:1px solid #253747;border-radius:24px;padding:25px;box-shadow:0 18px 60px #0005}
.tag{display:inline-block;padding:7px 11px;border-radius:30px;background:#203027;color:var(--green);font-size:11px;font-weight:bold}
h1{font-size:32px;margin:18px 0 8px}
p{color:var(--muted);line-height:1.6}
.center{text-align:center}
.power{margin:28px auto 20px;width:145px;height:145px;border-radius:50%;border:2px solid var(--green);background:#10271f;color:var(--green);font-size:45px;display:grid;place-items:center;cursor:pointer;box-shadow:0 0 30px #00e68a18}
.power:active{transform:scale(.97)}
button,select{font:inherit}
select{width:100%;padding:14px;background:#0b131e;color:white;border:1px solid #314355;border-radius:12px;margin:10px 0 18px}
.label{display:block;text-align:left;font-size:12px;color:var(--muted)}
.status{font-weight:bold;color:#ffd479}
.grid{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:24px}
.tile{padding:16px;background:#0b141f;border:1px solid #253747;border-radius:15px}
.tile small{display:block;color:var(--muted);margin-bottom:9px}
.tile strong{font-size:14px}
.green{color:var(--green)}
.notice{font-size:12px;background:#182431;padding:13px;border-radius:12px;margin-top:20px}
footer{text-align:center;padding:20px;color:#718397;font-size:12px}
</style>
</head>
<body>
<header>
  <div class="logo">M</div>
  <div>
    <div class="brand">MAX VPN MOZ</div>
    <div class="sub">SECURE CONNECTION</div>
  </div>
</header>

<main>
<section class="card center">
  <span class="tag">● INTERFACE DE DEMONSTRAÇÃO</span>
  <h1>A tua conexão.<br><span class="green">O teu controlo.</span></h1>
  <p>Um novo projeto VPN criado em Moçambique.</p>

  <button class="power" id="power" aria-label="Testar interface">⏻</button>
  <h3 id="state">Ainda não conectado</h3>
  <p id="detail">O servidor VPN ainda não está configurado.</p>

  <label class="label" for="server">LOCALIZAÇÃO DO SERVIDOR</label>
  <select id="server">
    <option value="mz">Moçambique — futuro servidor</option>
    <option value="global">Servidor global — por configurar</option>
  </select>

  <div class="grid">
    <div class="tile">
      <small>🛡️ PROTOCOLO</small>
      <strong>WireGuard</strong>
    </div>
    <div class="tile">
      <small>☁️ SERVIDOR</small>
      <strong id="serverStatus">Por configurar</strong>
    </div>
    <div class="tile">
      <small>🔐 SEGURANÇA</small>
      <strong>Planeada</strong>
    </div>
    <div class="tile">
      <small>📡 CONEXÃO</small>
      <strong id="connection">Inativa</strong>
    </div>
  </div>

  <div class="notice">
    ⚠️ Este botão só demonstra a interface. Não estabelece uma ligação VPN real nem fornece Internet.
  </div>
</section>
</main>

<footer>© 2026 MAX VPN MOZ · Projeto em desenvolvimento</footer>

<script>
const power = document.getElementById("power");
power.addEventListener("click", () => {
  document.getElementById("state").textContent =
    "Servidor ainda não configurado";
  document.getElementById("detail").textContent =
    "A interface funciona, mas precisas de um servidor VPN real para conectar.";
  document.getElementById("connection").textContent = "Inativa";
});
</script>
</body>
</html>
