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
<!-- halaman.html -->
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Ucapan Ulang Tahun</title>
  <link rel="stylesheet" href="style.css">
</head>
<body class="yellow-bg">
  <audio id="song" autoplay loop hidden>
    <source src="song.mp3" type="audio/mpeg">
    Browsermu tidak mendukung audio.
  </audio>

  <div class="container">
    <h1>Selamat Ulang Tahun! 🎉</h1>
    <p class="message">
      Hai, kam!<br><br>
      Di hari spesial ini, i just wanna say betapa bangganya punya teman sekuat dan sebaik kamil. Terima kasih sudah selalu ada, jadi sosok yang penuh semangat dan gak pernah menyerah meski dunia kadang berat banget. Kamila pantas banget buat semua kebahagiaan yang ada.<br><br>
      gua berdoa semoga semua impian kamila tercapai, semoga kamila selalu dikelilingi orang-orang baik, dan semoga kamila bisa terus jadi versi terbaik dari dirinya sendiri. Jangan pernah lupa kalau lu itu hebat dan layak dicintai! 💛<br><br>
      Selamat ulang tahun! 🎂
    </p>

    <button id="tombolKejutan">Tap Tap Tap</button>

    <div id="kejutan" class="hidden">
      <img src="https://media.giphy.com/media/3orieYQ4a8zwT8iA1G/giphy.gif" alt="Happy Birthday GIF">
    </div>
  </div>

  <script src="script.js"></script>
</body>
</html>
/* style.css */
body {
  margin: 0;
  padding: 0;
  font-family: 'Comic Sans MS', cursive, sans-serif;
  text-align: center;
}

.yellow-bg {
  background-color: #fff176;
  color: #333;
}

.container {
  padding: 50px;
  max-width: 700px;
  margin: auto;
  background-color: #fffde7;
  border-radius: 20px;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
  margin-top: 80px;
}

h1 {
  color: #fbc02d;
  font-size: 3em;
  margin-bottom: 20px;
}

.message {
  font-size: 1.2em;
  line-height: 1.6;
  color: #444;
}

input {
  padding: 10px;
  font-size: 1em;
  border-radius: 5px;
  border: 1px solid #ccc;
}

button {
  margin-top: 20px;
  padding: 15px 25px;
  font-size: 1em;
  background-color: #fdd835;
  color: #fff;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  transition: background 0.3s;
}

button:hover {
  background-color: #fbc02d;
}

.hidden {
  display: none;
}

img {
  width: 200px;
  margin-top: 20px;
  border-radius: 10px;
}

.error {
  color: red;
  margin-top: 10px;
}

