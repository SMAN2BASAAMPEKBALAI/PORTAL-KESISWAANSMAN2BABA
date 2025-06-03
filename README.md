# PORTAL-KESISWAANSMAN2BABA
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Login Portal Sekolah</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(to right, #2e86de, #54a0ff);
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }

    .login-box {
      background-color: white;
      padding: 30px;
      border-radius: 10px;
      width: 100%;
      max-width: 400px;
      box-shadow: 0 5px 15px rgba(0,0,0,0.3);
    }

    .login-box h2 {
      text-align: center;
      margin-bottom: 20px;
    }

    .form-group {
      margin-bottom: 15px;
    }

    .form-group label {
      display: block;
      margin-bottom: 5px;
      font-weight: bold;
    }

    .form-group input, .form-group select {
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
    <h2>Login Portal Sekolah</h2>
    <form onsubmit="login(event)">
      <div class="form-group">
        <label for="role">Login Sebagai:</label>
        <select id="role" required>
          <option value="">-- Pilih Peran --</option>
          <option value="siswa">Siswa</option>
          <option value="guru">Guru</option>
          <option value="admin">Admin</option>
        </select>
      </div>
      <div class="form-group">
        <label for="username">NIS / NIP / Username</label>
        <input type="text" id="username" placeholder="Masukkan ID Pengguna" required />
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
      const role = document.getElementById('role').value;
      const username = document.getElementById('username').value;
      const password = document.getElementById('password').value;

      // Simulasi login berdasarkan peran
      if (role === 'siswa' && username === 'siswa123' && password === 'siswa') {
        alert('Login siswa berhasil!');
        window.location.href = 'dashboard_siswa.html';
      } else if (role === 'guru' && username === 'guru123' && password === 'guru') {
        alert('Login guru berhasil!');
        window.location.href = 'dashboard_guru.html';
      } else if (role === 'admin' && username === 'admin123' && password === 'admin') {
        alert('Login admin berhasil!');
        window.location.href = 'dashboard_admin.html';
      } else {
        alert('Login gagal. Periksa kembali data Anda.');
      }
    }
  </script>
</body>
</html>
