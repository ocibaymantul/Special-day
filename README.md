# Special-day
<!-- index.html -->
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Selamat Ulang Tahun!</title>
  <link rel="stylesheet" href="style.css">
</head>
<body class="yellow-bg">
  <div class="container">
    <h1>Hi!</h1>
    <p>Masukkan kode rahasianya! (panggilanmu 3 huruf)</p>
    <input type="text" id="kode" placeholder="Contoh: kam">
    <button onclick="cekKode()">Masuk</button>
    <p id="error" class="error hidden">Kode salah! Coba lagi ya 😊</p>
  </div>

  <script>
    function cekKode() {
      const kode = document.getElementById("kode").value.toLowerCase();
      if (kode === "kam") {
        window.location.href = "halaman.html";
      } else {
        document.getElementById("error").classList.remove("hidden");
      }
    }
  </script>
</body>
</html>
