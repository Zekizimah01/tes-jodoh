<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Tes Jodoh Online</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .container {
      background: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.2);
      text-align: center;
      max-width: 400px;
      width: 100%;
    }

    input[type="text"] {
      width: 90%;
      padding: 10px;
      margin: 10px 0;
      border-radius: 10px;
      border: 1px solid #ccc;
      font-size: 16px;
    }

    button {
      background: #ff5e62;
      color: white;
      border: none;
      padding: 12px 24px;
      border-radius: 10px;
      font-size: 16px;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    button:hover {
      background: #ff3b3b;
    }

    .result {
      margin-top: 20px;
      font-size: 18px;
      font-weight: bold;
      color: #e91e63;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>💖 Tes Jodoh 💖</h2>
    <input type="text" id="nama1" placeholder="Masukkan Namamu" />
    <input type="text" id="nama2" placeholder="Masukkan Nama Dia" />
    <br />
    <button onclick="cekJodoh()">Tes Sekarang</button>
    <div class="result" id="hasil"></div>
  </div>

  <script>
    function cekJodoh() {
      const nama1 = document.getElementById("nama1").value.trim();
      const nama2 = document.getElementById("nama2").value.trim();
      const hasil = document.getElementById("hasil");

      if (nama1 === "" || nama2 === "") {
        hasil.innerText = "Masukkan kedua nama dulu ya!";
        return;
      }

      const persen = Math.floor(Math.random() * 51) + 50; // hasil 50% - 100%
      hasil.innerText = `${nama1} ❤️ ${nama2}\nKecocokan: ${persen}%`;
    }
  </script>
</body>
</html>
