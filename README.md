<!doctype html>
<html lang="it">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Colazione?</title>
  <style>
    :root { font-family: system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif; }
    body {
      margin: 0; min-height: 100svh; display: grid; place-items: center;
      background: #fff; color: #111;
    }
    .card {
      width: min(90vw, 520px);
      border: 1px solid #e5e7eb; border-radius: 16px; padding: 28px 24px;
      box-shadow: 0 10px 25px rgba(0,0,0,.06);
      text-align: center;
    }
    h1 { margin: 0 0 12px; font-size: 1.6rem; }
    p  { margin: 0 0 20px; color: #444; }
    .buttons { display: flex; gap: 12px; justify-content: center; flex-wrap: wrap; }
    button {
      cursor: pointer; border: 1px solid #111; background: #111; color: #fff;
      padding: 10px 16px; border-radius: 10px; font-size: 1rem; transition: transform .05s;
    }
    button:active { transform: translateY(1px); }
    .ghost { background: #fff; color: #111; }
    .result { margin-top: 18px; font-size: 1.8rem; min-height: 2em; }
  </style>
</head>
<body>
  <main class="card">
    <h1>colazione insieme mercoledì?</h1>
    <p>Scegli una risposta:</p>
    <div class="buttons">
      <button id="si">Sì</button>
      <button id="no" class="ghost">No</button>
    </div>
    <div id="result" class="result" aria-live="polite"></div>
  </main>

  <script>
    const res = document.getElementById('result');
    document.getElementById('si').addEventListener('click', () => {
      res.textContent = '😁😁😁😁';
    });
    document.getElementById('no').addEventListener('click', () => {
      res.textContent = 'ok👍';
    });

    // Facoltativo: apri direttamente con un dialogo iniziale
    // Se vuoi proprio un prompt all’apertura, scommenta qui sotto:
    /*
    window.addEventListener('load', () => {
      const risposta = confirm("colazione insieme mercoledì?");
      res.textContent = risposta ? '😁😁😁😁' : 'ok👍';
    });
    */
  </script>
</body>
</html>
