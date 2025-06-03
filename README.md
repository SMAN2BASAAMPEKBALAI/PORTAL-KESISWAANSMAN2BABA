# PORTAL-KESISWAANSMAN2BABA
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Login Sekolah</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: Arial, sans-serif;
      background-image: url(https://drive.google.com/file/d/1y762Gpqgs_Kut1mUCgALExAAFCarXFff/view?usp=drive_link);
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      margin: 0;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
    }

    body::before {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.5);
      z-index: 0;
    }

    .login-box {
      background-color: white;
      padding: 30px;
      border-radius: 10px;
      width: 100%;
      max-width: 400px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.5);
      text-align: center;
      position: relative;
      z-index: 1;
    }

    .logo {
      
      width: 100px;
      margin: 0 auto 20px auto;
      display: block;
    }

    .login-box h2 {
      margin-bottom: 20px;
    }

    .form-group {
      margin-bottom: 15px;
      text-align: left;
    }

    .form-group label {
      display: block;
      margin-bottom: 5px;
      font-weight: bold;
    }

    .form-group input {
      width: 100%;
      padding: 10px;
      border-radius: 5px;
      border: 1px solid #ccc;
    }

    .login-button {
      width: 100%;
      padding: 10px;
      background-color: #2e86de;
      color: white;
      border: none;
      border-radius: 5px;
      font-size: 16px;
      cursor: pointer;
    }

    .login-button:hover {
      background-color: #1e6fbd;
    }

    .footer {
      text-align: center;
      margin-top: 10px;
      font-size: 12px;
      color: #555;
    }
  </style>
</head>
<body>
  <div class="login-box">
    <img src="logo.png" alt="Logo Sekolah" class="logo" />
    <h2>Portal Login Sekolah</h2>
    <form onsubmit="login(event)">
      <div class="form-group">
        <label for="username">NIS / NIP</label>
        <input type="text" id="username" placeholder="Masukkan NIS/NIP" required />
      </div>
      <div class="form-group">
        <label for="password">Kata Sandi</label>
        <input type="password" id="password" placeholder="Masukkan Kata Sandi" required />
      </div>
      <button type="submit" class="login-button">Masuk</button>
    </form>
    <div class="footer">
      &copy; 2025 Portal Sekolah Digital
    </div>
  </div>

  <script>
    function login(event) {
      event.preventDefault();
      const username = document.getElementById('username').value;
      const password = document.getElementById('password').value;

      if (username === '199203212022032010' && password === 'fildzah2103') {
        alert('Login berhasil!');
        window.location.href = 'dashboard.html';
      } else {
        alert('NIS/NIP atau kata sandi salah.');
      }
    }
  </script>
</body>
</html>
