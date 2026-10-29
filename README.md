<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#080d14">
<title>MAX VPN MOZ</title>
<style>
:root {
  --green: #00e68a;
  --bg: #080d14;
  --panel: #111b28;
  --muted: #9aabba;
}
* { box-sizing: border-box; }
body {
  margin: 0;
  min-height: 100vh;
  color: white;
  background: radial-gradient(ellipse at top, #123326, var(--bg) 55%);
  font-family: Arial, sans-serif;
}
header {
  max-width: 900px;
  margin: auto;
  padding: 24px 20px;
  display: flex;
  align-items: center;
  gap: 12px;
}
.logo {
  width: 50px;
  height: 50px;
  border-radius: 15px;
  background: var(--green);
  color: #06130d;
  display: grid;
  place-items: center;
  font-size: 28px;
  font-weight: 900;
}
.brand { color: var(--green); font-size: 20px; font-weight: 900; }
.sub { color: var(--muted); font-size: 10px; letter-spacing: 2px; margin-top: 5px; }
main { max-width: 540px; margin: 25px auto; padding: 16px; }
.card {
  background: var(--panel);
  border: 1px solid #263b49;
  border-radius: 24px;
  padding: 25px 20px;
  box-shadow: 0 20px 60px #0005;
}
.center { text-align: center; }
.tag {
  display: inline-block;
  padding: 8px 12px;
  border-radius: 30px;
  background: #203027;
  color: var(--green);
  font-size: 11px;
  font-weight: bold;
}
h1 { font-size: 31px; line-height: 1.25; margin: 22px 0 10px; }
p { color: var(--muted); line-height: 1.6; }
.green { color: var(--green); }
.power {
  width: 140px;
  height: 140px;
  margin: 25px auto 15px;
  border-radius: 50%;
  border: 2px solid var(--green);
  background: #10271f;
  color: var(--green);
  font-size: 45px;
  display: grid;
  place-items: center;
  cursor: pointer;
  box-shadow: 0 0 30px #00e68a20;
}
.power:active { transform: scale(.97); }
.status { font-weight: bold; color: #ffd479; }
label {
  display: block;
  text-align: left;
  font-size: 12px;
  color: var(--muted);
  margin-top: 25px;
}
select {
  width: 100%;
  padding: 14px;
  margin-top: 10px;
  border: 1px solid #314355;
  border-radius: 12px;
  background: #0b131e;
  color: white;
}
.grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-top: 24px; }
.tile { padding: 15px; background: #0b141f; border: 1px solid #253747; border-radius: 15px; text-align: left; }
.tile small { display: block; color: var(--muted); margin-bottom: 9px; }
.tile strong { font-size: 14px; }
.notice { margin-top: 20px; padding: 13px; background: #182431; border-radius: 12px; text-align: left; font-size: 12px; color: #c1ced9; line-height: 1.6; }
footer { text-align: center; padding: 20px; color: #718397; font-size: 12px; }
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
    <span class="tag">● PROJETO EM DESENVOLVIMENTO</span>
    <h1>A tua conexão.<br><span class="green">O teu controlo.</span></h1>
    <p>Um novo projeto VPN criado para ligações seguras.</p>

    <button class="power" id="power" aria-label="Testar interface">⏻</button>
    <h3 id="state">Ainda não conectado</h3>
    <p id="detail">O servidor VPN ainda não está configurado.</p>

    <label for="server">LOCALIZAÇÃO DO SERVIDOR</label>
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
        <strong>Por configurar</strong>
      </div>
      <div class="tile">
        <small>📡 CONEXÃO</small>
        <strong id="connection">Inativa</strong>
      </div>
    </div>

    <div class="notice">
      ⚠️ Esta é uma interface de demonstração. O botão não estabelece uma ligação VPN real. É necessário configurar um servidor VPN para conectar.
    </div>
  </section>
</main>

<footer>© 2026 MAX VPN MOZ · Projeto em desenvolvimento</footer>

<script>
document.getElementById("power").addEventListener("click", function () {
  document.getElementById("state").textContent =
    "Servidor ainda não configurado";
  document.getElementById("detail").textContent =
    "A interface está pronta para o próximo passo.";
  document.getElementById("connection").textContent = "Inativa";
});
</script>
</body>
</html>
