<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>العبها صح</title>
  <style>
    body {
      margin: 0;
      font-family: 'Tajawal', sans-serif;
      background: linear-gradient(to bottom, #e0f7ff, #ffffff);
    }
    .start-screen {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: url('SXB (1).png') center center / cover no-repeat;
      text-align: center;
    }
    .start-screen h1 {
      font-size: 48px;
      color: #006fa6;
      margin-bottom: 20px;
    }
    .start-screen button {
      background-color: #006fa6;
      color: white;
      padding: 15px 30px;
      font-size: 20px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }
    .categories-page {
      display: none;
      padding: 40px;
      text-align: center;
    }
    .category-group {
      margin-bottom: 30px;
    }
    .category-group h2 {
      color: #006fa6;
      margin-bottom: 10px;
    }
    .categories {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
    }
    .category {
      background-color: #d6f0ff;
      border: 2px solid #006fa6;
      border-radius: 10px;
      padding: 10px 20px;
      font-size: 18px;
      cursor: pointer;
      transition: background 0.3s;
    }
    .category.selected {
      background-color: #a4e0ff;
    }
  </style>
</head>
<body>
  <div class="start-screen" id="startScreen">
    <h1>العبها صح</h1>
    <button onclick="goToCategories()">اختر الفئات</button>
  </div>

  <div class="categories-page" id="categoriesPage">
    <div class="category-group">
      <h2>مسلسلات</h2>
      <div class="categories">
        <div class="category">شارع الأعشى</div>
        <div class="category">شباب البومب</div>
        <div class="category">خريف القلب</div>
        <div class="category">خمس نجوم</div>
      </div>
    </div>
    <div class="category-group">
      <h2>إسلامي</h2>
      <div class="categories">
        <div class="category">إسلامي</div>
        <div class="category">قرآن</div>
        <div class="category">قصص الأنبياء</div>
        <div class="category">من القارئ</div>
      </div>
    </div>
    <div class="category-group">
      <h2>دول</h2>
      <div class="categories">
        <div class="category">خرائط</div>
        <div class="category">أعلام</div>
        <div class="category">عواصم</div>
        <div class="category">عملات</div>
        <div class="category">جغرافيا</div>
      </div>
    </div>
    <div class="category-group">
      <h2>عام</h2>
      <div class="categories">
        <div class="category">عالم الشعر</div>
        <div class="category">منتجات</div>
        <div class="category">من المشهور</div>
        <div class="category">سيارات</div>
        <div class="category">سوبرماركت</div>
      </div>
    </div>
    <div class="category-group">
      <h2>أنمي</h2>
      <div class="categories">
        <div class="category">ناروتو</div>
        <div class="category">هجوم العمالقة</div>
      </div>
    </div>
  </div>

  <script>
    function goToCategories() {
      document.getElementById('startScreen').style.display = 'none';
      document.getElementById('categoriesPage').style.display = 'block';
    }

    const categories = document.querySelectorAll('.category');
    let selectedCount = 0;

    categories.forEach(cat => {
      cat.addEventListener('click', () => {
        if (cat.classList.contains('selected')) {
          cat.classList.remove('selected');
          selectedCount--;
        } else if (selectedCount < 5) {
          cat.classList.add('selected');
          selectedCount++;
        }
      });
    });
  </script>
</body>
</html>

العــبها صــح
