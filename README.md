<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-widt  h, initial-scale=1.0"/>
  <title>Orozco's Registration Form</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #43cea2, #ed1b76);
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }

    .form-container {
      background: #037a76;
      padding: 40px 50px;
      border-radius: 15px;
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
      max-width: 400px;
      width: 100%;
    }

    .form-container h2 {
      text-align: center;
      color: #185a9d;
      margin-bottom: 30px;
    }

    .form-group {
      position: relative;
      margin-bottom: 25px;
    }

    .form-group input,
    .form-group select {
      width: 100%;
      padding: 12px;
      border: 1px solid #ed1b76;
      border-radius: 6px;
      font-size: 14px;
      outline: none;
    }

    .form-group label {
      position: absolute;
      top: -21px;
      left: 10px;
      background: #43cea2;
      padding: 0 5px;
      font-size: 15px;
      color: #000000;
    }

    /* Gender group override styles */
    .gender-group label {
      position: static;
      margin-bottom: 5px;
      font-size: 14px;
      color: #333;
    }

    .gender-options {
      display: flex;
      justify-content: small space-between;
      margin-top: 5px;
    }

    .gender-options label {
      font-size: 16px;
      color: #000000;
      display: flex;
      align-items: center;
    }

    .gender-options input {
      margin-right: 5px;
    }

    .button-group {
      display: flex;
      justify-content: space-between;
      gap: 10px;
    }

    .button-group button {
      flex: 1;
      padding: 12px;
      border: none;
      border-radius: 6px;
      font-size: 16px;
      cursor: pointer;
      transition: 0.3s;
    }

    .submit-btn {
      background-color: #43cea2;
      color: #fff;
    }

    .submit-btn:hover {
      background-color: #36a88e;
    }

    .reset-btn {
      background-color: #f55454;
      color: #fff;
    }

    .reset-btn:hover {
      background-color: #d94444;
    }

    @media (max-width: 480px) {
      .form-container {
        padding: 30px 20px;
      }

      .gender-options {
        flex-direction: column;
        gap: 5px;
      }
    }
  </style>
</head>
<body>

  <div class="form-container">
    <h2><p style="color: #f44786; background-color: #ffffff; text-align:center">Registration Portal</p></h2>
    <form onsubmit="return validateForm()">

      <div class="form-group">
        <label for="fullname">Full Name</label>
        <input type="text" id="fullname" name="fullname" required>
      </div>

      <div class="form-group">
        <label for="birthday">Birthday</label>
        <input type="date" id="birthday" name="birthday" required>
      </div>

      <div class="form-group">
        <label for="email">Email Address</label>
        <input type="email" id="email" name="email" required>
      </div>

      <div class="form-group">
        <label for="username">Username</label>
        <input type="text" id="username" name="username" required>
      </div>

      <div class="form-group">
        <label for="password">Password</label>
        <input type="password" id="password" name="password" required>
      </div>

      <div class="form-group">
        <label for="confirm-password">Confirm Password</label>
        <input type="password" id="confirm-password" name="confirm_password" required>
      </div>

      <div class="form-group gender-group">
        <label>Gender</label>
        <div class="gender-options">
          <label><input type="radio" name="gender" value="Male" required> Male</label>
          <label><input type="radio" name="gender" value="Female" required> Female</label>
        </div>
      </div>

      <div class="button-group">
        <button type="submit" class="submit-btn">Register</button>
        <button type="reset" class="reset-btn">Reset</button>
      </div>

    </form>
  </div>

  <script>
    function validateForm() {
      const password = document.getElementById('password').value;
      const confirmPassword = document.getElementById('confirm-password').value;

      if (password !== confirmPassword) {
        alert('❌ Passwords do not match!');
        return false;
      }

      alert('🎉 "Welcome, players. You will be playing games for money"🦑🟩 🟥 🎮  ');
      return true;
    }
  </script>

</body>
</html>
