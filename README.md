# Elfrgany
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تسجيل الدخول - elfrgany</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="login-container">
        <h2>تسجيل الدخول</h2>
        <form id="loginForm">
            <label for="username">اسم المستخدم:</label>
            <input type="text" id="username" name="username" required><br>

            <label for="password">كلمة المرور:</label>
            <input type="password" id="password" name="password" required><br>

            <button type="submit">تسجيل الدخول</button>
        </form>
        <p id="error-message" style="color: red; display: none;">اسم المستخدم أو كلمة المرور غير صحيحة.</p>
    </div>

    <script src="login.js"></script>
</body>
</html>
