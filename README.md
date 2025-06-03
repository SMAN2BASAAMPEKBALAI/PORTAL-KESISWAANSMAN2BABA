<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Dashboard SMA Negeri 2 Basa Ampek Balai</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: white;
      background-image: url('https://drive.google.com/uc?export=view&id=1y762Gpqgs_Kut1mUCgALExAAFCarXFff');
      background-size: cover;
      background-position: center;
      color: black;
    }
    .overlay {
      background-color: rgba(255, 255, 255, 0.7);
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
    }
    .container {
      position: relative;
      z-index: 2;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 20px;
    }
    .logo {
      width: 120px;
      margin-bottom: 20px;
    }
    .dashboard {
      background: rgba(255, 255, 255, 0.9);
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 0 10px #ccc;
      width: 100%;
      max-width: 400px;
    }
    h1 {
      text-align: center;
      color: #333;
    }
    label, select, input {
      display: block;
      width: 100%;
      margin-top: 10px;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    select, input {
      background: #f9f9f9;
      color: #000;
    }
    button {
      margin-top: 20px;
      padding: 10px;
      background: #00cc66;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-weight: bold;
    }
    button:hover {
      background: #00994d;
    }
  </style>
</head>
<body>
  <div class="overlay"></div>
  <div class="container">
    <h1 class="dashboard-title">Dashboard SMA Negeri 2 Basa Ampek Balai</h1>
    <div class="dashboard">
      <h1>Login Dashboard</h1>
      <form id="loginForm">
        <label for="role">Masuk sebagai:</label>
        <select id="role" required>
          <option value="">Pilih peran</option>
          <option value="siswa">Siswa</option>
          <option value="guru">Guru</option>
          <option value="admin">Admin</option>
        </select>

        <label for="username">Username:</label>
        <input type="text" id="username" required />

        <label for="password">Password:</label>
        <input type="password" id="password" required />

        <button type="submit">Masuk</button>
      </form>
        <p style="margin-top: 15px; text-align: center;">Belum punya akun? <a href="#" onclick="showRegister()">Buat akun</a></p>
      </div>

  <div class="container" id="registerContainer" style="display: none;">
    <div class="dashboard">
      <h1>Buat Akun</h1>
      <form id="registerForm">
        <label for="regRole">Daftar sebagai:</label>
        <select id="regRole" required>
          <option value="">Pilih peran</option>
          <option value="siswa">Siswa</option>
          <option value="guru">Guru</option>
        </select>

        <label for="regUsername">Username:</label>
        <input type="text" id="regUsername" required />

        <label for="regPassword">Password:</label>
        <input type="password" id="regPassword" required />

        <label for="regConfirmPassword">Konfirmasi Password:</label>
        <input type="password" id="regConfirmPassword" required />

        <button type="submit">Daftar</button>
        <p style="margin-top: 15px; text-align: center;"><a href="#" onclick="showLogin()">Sudah punya akun? Masuk di sini</a></p>
      </form>
    </div>
  </div>

  <script>
    document.getElementById("loginForm").addEventListener("submit", function (e) {
      e.preventDefault();
      const role = document.getElementById("role").value;
      const username = document.getElementById("username").value;
      const password = document.getElementById("password").value;

      if (role && username && password) {
        alert(`Login berhasil sebagai ${role.toUpperCase()}`);
        // Di sini bisa diarahkan ke dashboard sebenarnya
      } else {
        alert("Harap isi semua kolom!");
      }
    });
      function showRegister() {
      document.querySelector("#registerContainer").style.display = "flex";
      document.querySelector(".container").style.display = "none";
    }

    function showLogin() {
      document.querySelector("#registerContainer").style.display = "none";
      document.querySelector(".container").style.display = "flex";
    }

    document.getElementById("registerForm").addEventListener("submit", function (e) {
      e.preventDefault();
      const role = document.getElementById("regRole").value;
      const username = document.getElementById("regUsername").value;
      const password = document.getElementById("regPassword").value;
      const confirmPassword = document.getElementById("regConfirmPassword").value;

      if (password !== confirmPassword) {
        alert("Password tidak cocok!");
        return;
      }

      if (role && username && password) {
        alert(`Akun berhasil dibuat untuk ${role.toUpperCase()}`);
        showLogin();
      } else {
        alert("Harap isi semua kolom!");
      }
    });
  </script>
</body>
</html>
