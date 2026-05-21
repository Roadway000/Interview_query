# 🚀 IT Interview Trainer (Тренажер для Співбесід)

An interactive web application for preparing for technical interviews in IT disciplines. The application is completely static, works without a backend, and uses a structured database of questions in JSON format.
(Інтерактивний вебдодаток для підготовки до технічних співбесід з IT-дисциплін. Додаток є повністю статичним, працює без бекенду та використовує структуровану базу запитань у форматі JSON.)

🔗 **[ЖИВИЙ ДЕМО-САЙТ НА GITHUB PAGES](https://roadway000.github.io/Interview_query/)**

---

## 🌟 Features (Ключові фічі)
* **Saving the state of answers:** When switching between questions ("Back" / "Forward"), the application remembers your choice, blocks repeated clicks to avoid overcharging, and highlights the results.
* **Interactive feedback:** Instant semi-transparent highlighting of answers (green - correct, red - error) and automatic display of a detailed explanation next to the question.
* **Flexible filtering system:** Search by 8 different parameters simultaneously (topic, difficulty, question code, text, options, tags, source, etc.) thanks to dynamic `oninput` filters on the client side.
* **Fixed UI:** The navigation bar is fixed at the top, which prevents the interface from "jumping" when changing the length of the question text.
(* **Збереження стану відповідей:** При переході між запитаннями («Назад» / «Вперед») додаток пам'ятає ваш вибір, блокує повторні кліки, щоб не накручувати рахунок, і підсвічує результати.
* **Інтерактивний фідбек:** Миттєве напівпрозоре підсвічування відповідей (зелений — правильно, червоний — помилка) та автоматичне відображення детального пояснення (`explanation`) поруч із питанням.
* **Гнучка система фільтрації:** Пошук за 8 різними параметрами одночасно (тема, складність, код питання, текст, варіанти, теги, джерело тощо) завдяки динамічним `oninput` фільтрам на клієнтській стороні.
* **Фіксований UI:** Панель навігації закріплена у верхній частині, що запобігає «стрибанню» інтерфейсу під час зміни довжини тексту запитань.)

---

## 🛠️ Tech Stack (Стек технологій)
* **Frontend:** HTML5, CSS3 (CSS Variables, CSS Grid, Flexbox), JavaScript (Vanilla ES6)
* **Data Source:** Local JSON file (`Interview_query.json`) with detailed meta information for each question
* (Локальний JSON-файл (`Interview_query.json`) з детальною мета-інформацією для кожного запитання)
* **Хостинг:** GitHub Pages automatic deployment from the `main` branch
* (автоматичний деплой з гілки `main`)
* **IDE:** PyCharm 2025.2.4

---

## 📂 JSON Schema (Структура даних запитання)
Each question in the `Interview_query.json` file has a strongly typed structure:
(Кожне запитання у файлі `Interview_query.json` має строгу типізовану структуру:)
```json
{
  "id": "sql-fin-021",
  "topic": "SQL",
  "question_code": "SQL-DWH-16",
  "difficulty": "Intermediate",
  "question_text": "Яка схема даних у сховищах (Data Warehouse)...?",
  "options": [
    { "option_id": "a", "text": "Сніжинка (Snowflake)" },
    { "option_id": "b", "text": "Зірка (Star Schema)" }
  ],
  "correct_answer_id": "b",
  "explanation": "Схема 'Зірка' є найпростішою для розуміння...",
  "metadata": {
    "source": "Data Modeling Standards",
    "tags": ["SQL", "DWH", "Architecture"]
  }
}
