<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <title>Sevgilim Olur musun?</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      background: #ffe6f0;
      text-align: center;
    }
    h1 {
      font-size: 2em;
      color: #d63384;
      margin-bottom: 30px;
    }
    .buttons {
      display: flex;
      gap: 20px;
    }
    button {
      padding: 12px 24px;
      font-size: 1.1em;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: all 0.2s ease;
    }
    .yes {
      background-color: #4caf50;
      color: white;
    }
    .no {
      background-color: #f44336;
      color: white;
    }
    .message {
      margin-top: 30px;
      font-size: 1.4em;
      color: #4caf50;
    }
  </style>
</head>
<body>

  <h1 id="question">Benim sevgilim olur musun Eminamm?</h1>

  <div class="buttons" id="buttonContainer">
    <button class="yes" onclick="cevapEvet()">Evet</button>
    <button class="no" onclick="cevapHayir()">Hayır</button>
  </div>

  <div class="buttons" id="eminMisinButtons" style="display:none;">
    <p class="message" id="eminText">Emin misin?</p>
    <div style="display: flex; gap: 20px; margin-top: 10px;">
      <button class="yes" onclick="cevapEvet()">Evet</button>
    </div>
  </div>

  <p class="message" id="sonuc" style="display:none;"></p>

  <script>
    function cevapEvet() {
      document.getElementById("question").style.display = "none";
      document.getElementById("buttonContainer").style.display = "none";
      document.getElementById("eminMisinButtons").style.display = "none";
      document.getElementById("sonuc").innerText = "Evet diyeceğini biliyordum, sadece sormak istedim :)";
      document.getElementById("sonuc").style.display = "block";
    }

    function cevapHayir() {
      document.getElementById("buttonContainer").style.display = "none";
      document.getElementById("eminMisinButtons").style.display = "block";
    }
  </script>

</body>
</html>
