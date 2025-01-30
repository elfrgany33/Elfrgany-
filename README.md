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
<!DOCTYPE html>
<html>
<head>
<title>نموذج تسجيل طالب</title>
</head>
<body>

  <h2>تسجيل طالب</h2>

  <form action="process_registration.php" method="post">
    <label for="name">الاسم:</label><br>
    <input type="text" id="name" name="name" required><br><br>

    <label for="age">العمر:</label><br>
    <input type="number" id="age" name="age" min="1" required><br><br>

    <label for="parent_name">اسم ولي الأمر:</label><br>
    <input type="text" id="parent_name" name="parent_name" required><br><br>

    <label for="grade">المرحلة الدراسية:</label><br>
    <select id="grade" name="grade" required>
      <option value="first_secondary">الصف الأول الثانوي</option>
      <option value="second_secondary">الصف الثاني الثانوي</option>
      <option value="third_secondary">الصف الثالث الثانوي</option>
    </select><br><br>

    <label for="governorate">المحافظة:</label><br>
    <select id="governorate" name="governorate" required>
      <option value="القاهرة">القاهرة</option>
      <option value="الجيزة">الجيزة</option>
      <option value="الإسكندرية">الإسكندرية</option>
      {أضف بقية محافظات مصر هنا}
    </select><br><br>

    <input type="submit" value="تسجيل">
  </form>

</body>
</html>
<!DOCTYPE html>
<html>
<head>
  <title>منصة elfrgany التعليمية</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <img src="logo.png" alt="شعار elfrgany">
    <nav>
      <a href="courses.html">الدورات</a>
      <a href="materials.html">المواد</a>
      <a href="tests.html">الاختبارات</a>
      <a href="forum.html">المنتدى</a>
    </nav>
  </header>

  <main>
    <section id="about">
      <h2>مرحباً بكم في منصة elfrgany التعليمية</h2>
      <p>منصة تعليمية شاملة تسعى لتقديم تعليم متميز للطلاب في مختلف المراحل.</p>
    </section>

    <section id="featured-courses">
      <h2>أحدث الدورات</h2>
      <div class="course">
        <img src="course1.jpg" alt="صورة الدورة">
        <h3>دورة في الرياضيات</h3>
        <a href="course_details.html">عرض التفاصيل</a>
      </div>
      {المزيد من الدورات}
    </section>
  </main>

  <footer>
    <p>جميع الحقوق محفوظة &copy; 2024</p>
  </footer>
</body>
</html>
<!DOCTYPE html>
<html>
<head>
  <title>عنوان الفيديو - منصة elfrgany</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    {شعار الموقع، روابط الأقسام}
  </header>

  <main>
    <section id="video-area">
      <h2>عنوان الفيديو</h2>
      <video controls>
        <source src="video.mp4" type="video/mp4">
        متصفحك لا يدعم تشغيل الفيديو.
      </video>
      <p>وصف الفيديو: شرح موجز لمحتوى الفيديو وأهميته.</p>
    </section>

    <section id="related-materials">
      <h3>مواد تعليمية مرتبطة</h3>
      <ul>
        <li><a href="file.pdf">ملف PDF</a></li>
        <li><a href="link">رابط لمصدر خارجي</a></li>
      </ul>
    </section>

    <section id="comments">
      <h3>التعليقات</h3>
      {نظام التعليقات}
    </section>
  </main>

  <footer>
    {حقوق النشر}
  </footer>
</body>
</html>
