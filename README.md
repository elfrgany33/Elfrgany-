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
import sqlite3

# إنشاء قاعدة البيانات والاتصال بها
conn = sqlite3.connect('people.db')
c = conn.cursor()

# إنشاء جدول لتخزين بيانات الأشخاص
c.execute('''
    CREATE TABLE IF NOT EXISTS person (
        id INTEGER PRIMARY KEY AUTOINCREMENT,
        name TEXT NOT NULL,
        age INTEGER NOT NULL,
        email TEXT NOT NULL
    )
''')

# دالة لتسجيل بيانات شخص
def register_person(name, age, email):
    c.execute('''
        INSERT INTO person (name, age, email)
        VALUES (?, ?, ?)
    ''', (name, age, email))
    conn.commit()
    print(f'Person {name} registered successfully')

# مثال على استخدام الدالة
register_person('John Doe', 30, 'john.doe@example.com')

# إغلاق الاتصال بقاعدة البيانات
conn.close()
