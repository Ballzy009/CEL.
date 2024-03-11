<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login and Sign Up Page</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background-color: #f5f5f5;
      margin: 0;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
    }

    main {
      background-color: #fff;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
      padding: 20px;
      width: 300px;
      text-align: center;
    }

    header {
      background-color: #3498db;
      color: #fff;
      padding: 10px;
      border-radius: 4px;
      margin-bottom: 20px;
    }

    form {
      display: flex;
      flex-direction: column;
    }

    .form_wrapper {
      position: relative;
      margin-bottom: 20px;
    }

    input {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      border: 1px solid #ccc;
      border-radius: 4px;
      box-sizing: border-box;
    }

    label {
      position: absolute;
      top: 12px;
      left: 10px;
      font-size: 12px;
      color: #777;
      pointer-events: none;
      transition: 0.3s;
    }

    input:focus+label,
    input:valid+label {
      top: 0;
      font-size: 10px;
      color: #3498db;
    }

    .material-icons {
      position: absolute;
      top: 20px;
      right: 10px;
      color: #777;
    }

    .remember_box {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 20px;
    }

    .remember {
      display: flex;
      align-items: center;
    }

    button {
      background-color: #3498db;
      color: #fff;
      padding: 10px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-size: 14px;
    }

    .new_account {
      margin-top: 20px;
      font-size: 12px;
    }

    a {
      color: #3498db;
      text-decoration: none;
      font-weight: bold;
    }
  </style>
</head>

<body>
  <main>
    <header>
      <h4>Login</h4>
    </header>
    <form>
      <div class="form_wrapper">
        <input id="input" type="text" required>
        <label for="input">Username</label>
        <i class="material-icons">person</i>
      </div>
      <div class="form_wrapper">
        <input id="password" type="password" required>
        <label for="password">Password</label>
        <i class="material-icons">lock</i>
      </div>
      <div class="remember_box">
        <div class="remember">
          <input type="checkbox">
          Remember me
        </div>
        <a href="#">Forgot Password ?</a>
      </div>
      <button>Login</button>
      <div class="new_account">
        Don't have an account? <a href="#">Sign up</a>
      </div>
    </form>

    <!-- Sign Up Form -->
    <form style="display: none;">
      <div class="form_wrapper">
        <input id="signup_username" type="text" required>
        <label for="signup_username">Username</label>
      </div>
      <div class="form_wrapper">
        <input id="signup_email" type="email" required>
        <label for="signup_email">Email</label>
      </div>
      <div class="form_wrapper">
        <input id="signup_password" type="password" required>
        <label for="signup_password">Password</label>
      </div>
      <button>Sign Up</button>
    </form>
  </main>

  <script>
    const loginForm = document.querySelector('form');
    const signUpForm = document.querySelectorAll('form')[1];
    const signUpLink = document.querySelector('.new_account a');

    signUpLink.addEventListener('click', function (e) {
      e.preventDefault();
      loginForm.style.display = 'none';
      signUpForm.style.display = 'flex';
    });
  </script>
</body>

</html>
