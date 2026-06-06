# 🚀 IT Interview Trainer (Тренажер для Співбесід)

An interactive web application for preparing for technical interviews in IT disciplines. The application is completely static, works without a backend, uses a structured database of questions in JSON format, and intelligently saves state using LocalStorage.
(Інтерактивний вебдодаток для підготовки до технічних співбесід з IT-дисциплін. Додаток є повністю статичним, працює без бекенду, використовує структуровану базу запитань у форматі JSON та розумно зберігає свій стан через LocalStorage.)

🔗 **[ЖИВИЙ ДЕМО-САЙТ НА GITHUB PAGES](https://roadway000.github.io/Interview_query/)**

---

## 🌟 Features (Ключові фічі)

* **💾 Full Progress Retention (Збереження прогресу тесту):** Application automatically saves all your answers, score, and the exact question you stopped on inside browser's `LocalStorage`. You can close your phone or PC browser, return days later, and continue exactly where you left off.
  (* **Повне збереження прогресу:** Додаток автоматично зберігає всі ваші відповіді, поточний рахунок та точний номер питання, на якому ви зупинилися, в `LocalStorage` браузера. Можна закрити вкладку на телефоні чи ПК, повернутися через кілька днів і продовжити з того самого місця.)
* **⏱️ Exam Countdown Timer (Таймер зворотного відліку):** Implements a realistic 2-hour exam simulation. The timer ticks automatically when the window is active, freezes safely when the tab is closed, and resumes upon return.
  (* **Таймер реального іспиту:** Вбудовано зворотний відлік на 2 години для симуляції справжнього тестування. Таймер працює, поки вкладка активна, «заморожується» при закритті сторінки та продовжується при повторному візиті.)
* **⚙️ Pop-up Admin & AI Panel (Прихована Адмінка та ШІ):** A clean, modal-driven control dashboard that doesn't distract during testing. It includes a ready-to-use prompt template for ChatGPT to generate compatible questions and lets you import them instantly on the fly.
  (* **Спливаюча Адмін-панель та ШІ:** Елегантне модальне вікно для керування контентом, яке не відволікає під час тесту. Містить готовий промпт-шаблон для ChatGPT для генерації сумісних питань та дозволяє миттєво імпортувати їх "на льоту".)
* **🔄 Custom Confirmation Dialogs (Витончені діалоги підтвердження):** Replaced default, scary browser alerts with highly stylized modal dialogs that dynamically warning users about resetting their specific score before clearing history.
  (* **Сучасні вікна підтвердження:** Стандартні застарілі сповіщення браузера замінено на красиві модальні вікна у стилі додатка, які динамічно попереджають користувача про втрату його конкретної кількості балів перед скиданням тесту.)
* **⌨️ Keyboard Navigation (Керування з клавіатури):** Supports lightning-fast switching between questions using `ArrowLeft` and `ArrowRight` keys, which automatically disables when typing inside the Admin panel.
  (* **Навігація клавіатурою:** Можливість миттєво гортати питання кнопками «Вліво» та «Вправо» на клавіатурі. Керування автоматично блокується, коли ви вводите текст в адмінці.)
* **🔎 Advanced Multi-Filtering (Гнучка система фільтрації):** Search by 8 parameters simultaneously (topic, difficulty, code, question text, options, explanation, source, metadata tags) with instant client-side rendering.
  (* **Гнучка фільтрація:** Одночасний пошук за 8 параметрами завдяки динамічним `oninput` фільтрам на клієнтській стороні.)

---

## 🛠️ Tech Stack (Стек технологій)
* **Frontend:** HTML5, CSS3 (CSS Variables, Flexbox, CSS Grid), Vanilla JavaScript (ES6, LocalStorage API, Keyboard Events)
* **Data Source:** Local JSON database (`Interview_query.json`) + dynamic LocalStorage extension layer for custom AI content.
* **Hosting:** GitHub Pages with automatic deployment from the `main` branch.
* **IDE:** PyCharm 2025.2.4

---

## 📂 JSON Schema (Структура даних запитання)
Each question in the `Interview_query.json` file (and AI generated arrays) must adhere to this typed structure:
(Кожне запитання у файлі має строгу типізовану структуру:)

```json
{
  "id": "sql-fin-021",
  "topic": "SQL",
  "question_code": "SQL-DWH-16",
  "difficulty": "Intermediate",
  "question_text": "What is the primary data schema in a classic Data Warehouse...?",
  "options": [
    { "option_id": "a", "text": "Snowflake Schema" },
    { "option_id": "b", "text": "Star Schema" }
  ],
  "correct_answer_id": "b",
  "explanation": "Star Schema is the simplest and most efficient layout for DWH querying...",
  "metadata": {
    "source": "Data Modeling Standards",
    "tags": ["SQL", "DWH", "Architecture"]
  }
}