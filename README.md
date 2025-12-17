<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Delivery PRO – Painel</title>
  <meta name="theme-color" content="#0f172a" />
  <style>
    body { margin:0; font-family: Arial, Helvetica, sans-serif; background:#0f172a; color:#fff; }
    header { background:#020617; padding:15px; text-align:center; font-size:20px; font-weight:bold; }
    nav { display:flex; justify-content:space-around; background:#020617; padding:10px; }
    nav button { background:#1e293b; border:none; color:#fff; padding:10px; border-radius:8px; width:100%; margin:5px; }
    section { padding:15px; }
    .card { background:#1e293b; padding:15px; border-radius:12px; margin-bottom:15px; }
    .hidden { display:none; }
    input, select { width:100%; padding:10px; border-radius:8px; border:none; margin-top:8px; }
    .btn { background:#22c55e; color:#000; padding:12px; border:none; border-radius:10px; margin-top:10px; width:100%; font-weight:bold; }
    .danger { background:#ef4444; color:#fff; }
  </style>
</head>
<body>

<header>🚀 Delivery PRO</header>

<nav>
  <button onclick="showPanel('admin')">Admin</button>
  <button onclick="showPanel('loja')">Loja</button>
  <button onclick="showPanel('entregador')">Entregador</button>
</nav>

<!-- PAINEL ADMIN -->
<section id="admin" class="card">
  <h2>👑 Painel Admin</h2>
  <p>Créditos: ♾️ <b>ILIMITADOS</b></p>
  <p>Taxa por entrega: <b>R$ 1,50</b></p>

  <h3>⚙️ Controle do Sistema</h3>
  <button class="btn danger">Bloquear Loja</button>
  <button class="btn danger">Remover Loja</button>
  <button class="btn danger">Bloquear Entregador</button>
  <button class="btn danger">Remover Entregador</button>

  <h3>Recarregar Loja</h3>
  <input placeholder="Nome da loja" />
  <input type="number" placeholder="Créditos" />
  <button class="btn">Recarregar</button>

  <h3>Resumo</h3>
  <p>Total de entregas: 0</p>
  <p>Lucro Admin: R$ 0,00</p>

  <h3>📊 Entregadores</h3>
  <div class="card">
    <p><b>Entregador:</b> João</p>
    <p>Entregas: 12</p>
    <p>KM rodados: 48 km</p>
    <p>Valor a pagar: <b>R$ 96,00</b></p>
    <button class="btn">Marcar como pago</button>
  </div>

  <div class="card">
    <p><b>Entregador:</b> Maria</p>
    <p>Entregas: 8</p>
    <p>KM rodados: 30 km</p>
    <p>Valor a pagar: <b>R$ 60,00</b></p>
    <button class="btn">Marcar como pago</button>
  </div>
</section>

<!-- PAINEL LOJA -->
<section id="loja" class="card hidden">
  <h2>🏪 Painel Loja</h2>
  <p>Créditos disponíveis: <b>100</b></p>

  <h3>Solicitar Entrega</h3>
  <input placeholder="Endereço de coleta" />
  <input placeholder="Endereço de entrega" />
  <select>
    <option>Entrega automática</option>
    <option>Escolher entregador</option>
  </select>
  <button class="btn">Solicitar</button>

  <button class="btn danger">Bloquear Entregador</button>
</section>

<!-- PAINEL ENTREGADOR -->
<section id="entregador" class="card hidden">
  <h2>🛵 Painel Entregador</h2>
  <p>Status: <b>Online</b></p>
  <p>Saldo da semana: <b>R$ 0,00</b></p>

  <div class="card">
    <p>📍 Nova entrega próxima</p>
    <button class="btn">Aceitar</button>
    <button class="btn danger">Recusar</button>
  </div>

  <button class="btn">Abrir Mapa</button>
</section>

<script>
  function showPanel(panel) {
    document.getElementById('admin').classList.add('hidden');
    document.getElementById('loja').classList.add('hidden');
    document.getElementById('entregador').classList.add('hidden');
    document.getElementById(panel).classList.remove('hidden');
  }
</script>

</body>
</html>
