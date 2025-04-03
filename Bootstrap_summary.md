# ملخص بسيط لمحاضرة ال Bootstrap

## مقدمة عن Bootstrap
Bootstrap هو إطار عمل (Framework) جاهز بيسهل عليك تصميم مواقع ويب متجاوبة بدون ما تكتب أكواد CSS معقدة.

### ليه نستخدم Bootstrap؟
- بيخلي الموقع متناسق على كل الأجهزة.
- بيحل مشاكل التصميم العادي في HTML وCSS.
- بيحتوي على مكونات جاهزة زي الأزرار والنماذج والقوائم.

## إعداد Bootstrap في المشروع
### 1. تحميل Bootstrap
ممكن تستخدمه بطريقتين:
- تحميل الملفات من الموقع الرسمي.
- استخدام CDN زي كده:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">
```

### 2. ربط الملفات في HTML
```html
<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>موقعي</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">
</head>
<body>
    <h1 class="text-center">أهلا بيك في Bootstrap!</h1>
</body>
</html>
```
- **text-center**: بيخلي النص في المنتصف.

[شوف تنفيذ الكود من هنا](https://codepen.io/Omar-Abouelkheir-the-selector/pen/GgRzeLa)
---

## نظام الجريد (Grid System)
Bootstrap بيعتمد على **نظام 12 عمود** لتقسيم الصفحة، وده بيساعدك تتحكم في توزيع المحتوى.

### أمثلة على استخدام الجريد
```html
<div class="container">
    <div class="row">
        <div class="col-md-4 bg-primary text-white">عمود 1</div>
        <div class="col-md-4 bg-secondary text-white">عمود 2</div>
        <div class="col-md-4 bg-success text-white">عمود 3</div>
    </div>
</div>
```
- **container**: بيحدد منطقة العمل وبيخلي المحتوى في المنتصف بعرض مناسب.
- **row**: بيحدد صف يحتوي على أعمدة.
- **col-md-4**: بيحدد إن العمود ياخد 4 من 12 (يعني 3 أعمدة في الصف).
- **bg-primary, bg-secondary, bg-success**: بتحدد لون الخلفية.
- **text-white**: بتخلي النص باللون الأبيض عشان يكون واضح على الخلفية.

[شوف تنفيذ الكود من هنا](https://codepen.io/Omar-Abouelkheir-the-selector/pen/mydvoYY)
---

## الأزرار (Buttons)
Bootstrap بيقدم أنواع وأحجام مختلفة من الأزرار.

### أمثلة على الأزرار
```html
<button class="btn btn-primary">زر رئيسي</button>
<button class="btn btn-secondary">زر ثانوي</button>
<button class="btn btn-success">زر ناجح</button>
<button class="btn btn-danger">زر تحذيري</button>
<button class="btn btn-warning">زر إنذار</button>
<button class="btn btn-info">زر معلومات</button>
```
- **btn**: بيحدد إن العنصر زر.
- **btn-primary, btn-secondary, btn-success, btn-danger, btn-warning, btn-info**: بتحدد لون الزر حسب نوعه.

[شوف تنفيذ الكود من هنا](https://codepen.io/Omar-Abouelkheir-the-selector/pen/JojxzQZ)
---

### تغيير حجم الأزرار
```html
<button class="btn btn-primary btn-lg">زر كبير</button>
<button class="btn btn-primary btn-sm">زر صغير</button>
```
- **btn-lg**: بيخلي الزر أكبر.
- **btn-sm**: بيخلي الزر أصغر.

---

## النماذج (Forms)
Bootstrap بيخلي النماذج شكلها احترافي وسهل الاستخدام.

### نموذج بسيط
```html
<form>
    <div class="mb-3">
        <label for="email" class="form-label">البريد الإلكتروني</label>
        <input type="email" class="form-control" id="email" placeholder="أدخل بريدك الإلكتروني">
    </div>
    <div class="mb-3">
        <label for="password" class="form-label">كلمة المرور</label>
        <input type="password" class="form-control" id="password" placeholder="********">
    </div>
    <button type="submit" class="btn btn-primary">إرسال</button>
</form>
```
- **mb-3**: بيضيف مسافة تحت العنصر (margin-bottom 3).
- **form-label**: بيحسن شكل تسمية الحقول.
- **form-control**: بيخلي المدخلات تاخد عرض كامل بشكل متناسق.

[شوف تنفيذ الكود من هنا](https://codepen.io/Omar-Abouelkheir-the-selector/pen/RNwvdXO)
---

## شريط التنقل (Navbar)
Bootstrap بيسهل عليك تعمل شريط تنقل احترافي.

### مثال على Navbar بسيط
```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">موقعي</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item"><a class="nav-link active" href="#">الرئيسية</a></li>
        <li class="nav-item"><a class="nav-link" href="#">خدماتنا</a></li>
        <li class="nav-item"><a class="nav-link" href="#">تواصل معنا</a></li>
      </ul>
    </div>
  </div>
</nav>
```
- **navbar**: بيحدد العنصر كقائمة تنقل.
- **navbar-expand-lg**: بيخلي القائمة أفقية على الشاشات الكبيرة وتتحول لقائمة منسدلة على الشاشات الصغيرة.
- **bg-light**: بيخلي الخلفية فاتحة.
- **navbar-toggler**: زر لفتح القائمة على الشاشات الصغيرة.
- **collapse navbar-collapse**: بيخلي القائمة تشتغل مع الزر في الموبايل.
- **nav-item, nav-link**: بتحدد عناصر القائمة.

[شوف تنفيذ الكود من هنا](https://codepen.io/Omar-Abouelkheir-the-selector/pen/gbOqEZJ)

---

## الصور (Images)
Bootstrap بيقدم تنسيقات جاهزة للصور.

### مثال على تنسيق الصور
```html
<img src="image.jpg" class="img-fluid" alt="صورة متجاوبة">
<img src="image.jpg" class="rounded" alt="صورة بحواف دائرية">
<img src="image.jpg" class="img-thumbnail" alt="صورة بإطار">
```
- **img-fluid**: بيخلي الصورة متجاوبة وتأخذ عرض الحاوية.
- **rounded**: بيضيف حواف دائرية للصورة.
- **img-thumbnail**: بيضيف إطار للصورة.

---


## مصادر وأمثلة عملية
- الموقع الرسمي لـ Bootstrap: [https://getbootstrap.com](https://getbootstrap.com)
- أمثلة جاهزة من الموقع الرسمي: [https://getbootstrap.com/docs/5.3/examples/](https://getbootstrap.com/docs/5.3/examples/)