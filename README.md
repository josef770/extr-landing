<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>EXTR - כרטיסי טיסה</title>
  <style>
    body { font-family: Arial, sans-serif; background: #f9f9f9; margin: 0; padding: 0; }
    .container { max-width: 800px; margin: auto; background: white; padding: 30px; border-radius: 12px; box-shadow: 0 0 15px rgba(0,0,0,0.1); margin-top: 40px; }
    h1 { text-align: center; }
    form { display: grid; gap: 15px; direction: rtl; }
    input, select, button {
      font-size: 1rem; padding: 10px; border: 1px solid #ccc; border-radius: 8px;
    }
    button { background: #0a84ff; color: white; border: none; cursor: pointer; }
    .lang-switch { text-align: left; margin-bottom: 10px; }
    .lang-switch button { background: none; color: #0a84ff; border: none; cursor: pointer; font-weight: bold; }
    .footer { margin-top: 30px; font-size: 0.9em; text-align: center; color: #555; }
  </style>
  <script>
    function switchLang(lang) {
      if (lang === 'en') {
        document.body.setAttribute('dir', 'ltr');
        document.body.setAttribute('lang', 'en');
        location.href = '?lang=en';
      } else {
        document.body.setAttribute('dir', 'rtl');
        document.body.setAttribute('lang', 'he');
        location.href = '?lang=he';
      }
    }
  </script>
</head>
<body>
  <div class="container">
    <div class="lang-switch">
      <button onclick="switchLang('he')">עברית</button> | 
      <button onclick="switchLang('en')">English</button>
    </div>
    <h1>EXTR - רכישת כרטיסי טיסה</h1>
    <p>מלאו את הפרטים ונחזור אליכם עם הצעה משתלמת</p>
    <form>
      <input type="text" placeholder="שם לקוח" required>
      <input type="email" placeholder="אימייל" required>
      <input type="text" placeholder="טלפון" required>
      <input type="number" placeholder="כמה כרטיסים מדובר">
      <input type="text" placeholder="מאיפה לאן הטיסה">
      <select>
        <option>צד אחד</option>
        <option>הלוך וחזור</option>
        <option>מרובה יעדים</option>
      </select>
      <input type="text" placeholder="מה התאריכים">
      <input type="text" placeholder="מה הגמישות">
      <input type="text" placeholder="טיסה ישירה או עם עצירה">
      <button type="submit">שליחה</button>
    </form>
    <div class="footer">
      דוא"ל: d@ex2r.com | טלפון: 052-8337704
    </div>
  </div>
</body>
</html>
