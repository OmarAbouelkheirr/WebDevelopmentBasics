
# ملخص بسيط لل HTML

## يعني ايه HTML !
HTML هي اختصار لـ "HyperText Markup Language"، وهي لغة ترميزية تُستخدم لإنشاء وبناء صفحات الويب. تعتبر HTML الأساس الذي يعتمد عليه أي موقع ويب، حيث تسمح بتحديد الهيكل العام للمحتوى مثل النصوص، الصور، الروابط، والجداول. عن طريق HTML، يمكن للمطورين تحديد كيفية عرض المحتوى على المتصفحات. يتم استخدام HTML بشكل رئيسي مع تقنيات أخرى مثل CSS و JavaScript لتنسيق وتصميم الصفحات وإضافة التفاعل.

---

## التاجز الأساسية
| العلامة | الوظيفة | مثال |
|---------|---------|------|
| `<html>` | بتضم كل الصفحة | `<html>...</html>` |
| `<head>` | معلومات الصفحة | `<head>...</head>` |
| `<body>` | المحتوى الظاهر | `<body>...</body>` |
| `<title>` | عنوان الصفحة | `<title>موقعي</title>` |

---

## تنسيق النصوص:
```html
<h1>عنوان رئيسي</h1> <!-- من h1 ل h6 -->
<p>فقرة عادية</p>
<b>عريض</b> - <i>مائل</i> - <u>مسطر</u>
<br> <!-- سطر جديد -->
<hr> <!-- خط أفقي -->
```

## كود لصفحة بسيطة:
```html
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```

# القوائم (Lists)

## قايمة مرتبة:
- Tag name -> ol (Orderd List)

```html
<ol>
    <li>HTML</li>
    <li>CSS</li>
</ol>
```

## قايمة غير مرتبة:
- Tag name -> ul (Unordered  List)

```html
<ul>
    <li>HTML</li>
    <li>CSS</li>
</ul>
```

# الجداول في HTML

## الأساسيات
- الوسم الأساسي: `<table>` لإنشاء الجدول
- كل صف يُحدد بـ `<tr>` (Table Row)
- كل خلية بيانات تُحدد بـ `<td>` (Table Data)
- العناوين تُحدد بـ `<th>` (Table Header)

## مثال لجدول بسيط

```html
<table border="1">
  <tr>
    <th>الاسم</th>
    <th>العمر</th>
  </tr>
  <tr>
    <td>أحمد</td>
    <td>25</td>
  </tr>
</table>
```


## عندنا مثال تاني فيه شويه تفاصيل

```html
<table>
  <caption>عنوان الجدول</caption>
  <thead>
    <tr>
      <th>رأس العمود 1</th>
      <th>رأس العمود 2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>بيانات 1</td>
      <td>بيانات 2</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>مجموع 1</td>
      <td>مجموع 2</td>
    </tr>
  </tfoot>
</table>
```

## جدول خصائص الجداول

| الخاصية     | الوصف                                  | مثال               |
|------------|---------------------------------------|--------------------|
| `border`   | عرض حدود الجدول                       | `border="1"`       |
| `cellpadding` | المسافة بين محتوى الخلية وحوافها      | `cellpadding="5"`  |
| `cellspacing` | المسافة بين الخلايا المجاورة         | `cellspacing="0"`  |
| `width`    | عرض الجدول (بالبكسل أو النسبة المئوية) | `width="100%"`     |
| `colspan`  | عدد الأعمدة المدمجة                   | `colspan="2"`      |
| `rowspan`  | عدد الصفوف المدمجة                    | `rowspan="2"`      |

# الروابط (Links)

## رابط بسيط:
```html
<a href="https://www.example.com">اضغط هنا</a>
```

## روابط داخلية:
علشان نروح قسم فنفس الصفحة ( باستخدام الid )
```html
<a href="#section1">اذهب إلى القسم 1</a>
```
ده القسم الي هيروحله
```html
<h2 id="section1">القسم 1</h2>
```

## رابط بريد إلكتروني:
```html
<a href="omar@example.com">إرسل بريد</a>
```

# الصور (Images)

## علشان نحط صورة:
```html
<img src="image.jpg" alt="وصف الصورة" />
```

- `src`: المصدر أو مسار الصورة
- `alt`: نص بديل يظهر في حال عدم تحميل الصورة


# الفيديوهات (Videos)

## علشان نحط فيديو:
```html
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  متصفحك لا يدعم الفيديو.
</video>
```

# الملفات الصوتية (Audio)

## إضافة صوت:
```html
<audio controls>
  <source src="audio.mp3" type="audio/mp3">
  متصفحك لا يدعم الصوت.
</audio>
```

# النماذج (Forms)

## النموذج الأساسي:
```html
<form action="/submit" method="post">
  <label for="name">الاسم:</label>
  <input type="text" id="name" name="name">
  <input type="submit" value="إرسال">
</form>
```

## أنواع المدخلات:
- نص:
```html
<input type="text" />
```
- بريد إلكتروني:
```html
<input type="email" />
```
- كلمة مرور:
```html
<input type="password" />
```
- زر إرسال:
```html
<input type="submit" />
```

## قوائم منسدلة:
```html
<select>
  <option value="1">الخيار 1</option>
  <option value="2">الخيار 2</option>
</select>
```

# التنسيق باستخدام CSS

## إضافة CSS داخلي:
```html
<style>
  body {
    background-color: lightblue;
  }
  h1 {
    color: red;
  }
</style>
```

## إضافة CSS خارجي:
```html
<link rel="stylesheet" type="text/css" href="styles.css">
```

# التنسيق المتقدم

## إضافة فواصل (Breaks):
```html
<p>هذه فقرة تحتوي على <br> فاصل.</p>
```

## ال (Comments):
```html
<!-- هذه ملاحظة ولن تظهر في المتصفح -->
```

# حاجات تانيه مهمه:

## تقسيم الصفحة باستخدام الفئات (Divs) والأقسام (Sections):
```html
<div class="container">
  <h2>عنوان القسم</h2>
  <p>نص داخل قسم</p>
</div>
```

## تداخل العناصر:
```html
<div>
  <p>فقرة داخل ديف</p>
  <ul>
    <li>عنصر قائمة</li>
  </ul>
</div>
```
