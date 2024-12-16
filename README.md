# Mindfulspace
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MindfulSpace Login</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background: #f0f0f0;
        }
        .container {
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
        }
        .container h1 {
            font-size: 20px;
            margin-bottom: 20px;
        }
        input, button {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            background: #4caf50;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background: #45a049;
        }
        a {
            color: #007bff;
            text-decoration: none;
            font-size: 14px;
        }
        a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <div class="container" id="login-container">
        <h1>MindfulSpace Login</h1>
        <form id="login-form">
            <input type="email" id="login-email" placeholder="Email" required>
            <input type="password" id="login-password" placeholder="Password" required>
            <button type="submit">Login</button>
        </form>
        <a href="#" id="forgot-password-link">Forgot Password?</a>
    </div>

    <div class="container" id="forgot-password-container" style="display: none;">
        <h1>MindfulSpace Reset Password</h1>
        <form id="forgot-password-form">
            <input type="email" id="forgot-email" placeholder="Enter your email" required>
            <button type="submit">Reset</button>
        </form>
        <a href="#" id="back-to-login">Back to Login</a>
    </div>

    <script>
        const loginContainer = document.getElementById('login-container');
        const forgotPasswordContainer = document.getElementById('forgot-password-container');

        document.getElementById('forgot-password-link').addEventListener('click', (e) => {
            e.preventDefault();
            loginContainer.style.display = 'none';
            forgotPasswordContainer.style.display = 'block';
        });

        document.getElementById('back-to-login').addEventListener('click', (e) => {
            e.preventDefault();
            forgotPasswordContainer.style.display = 'none';
            loginContainer.style.display = 'block';
        });

        document.getElementById('login-form').addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Login submitted!');
        });

        document.getElementById('forgot-password-form').addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Password reset link sent!');
        });
    </script>
</body>
</html>
