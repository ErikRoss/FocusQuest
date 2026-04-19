# **🤝 Внесок у FocusQuest (Contributing)**

Вітаємо в Гільдії Розробників\! ⚔️ Ми дуже раді, що ви зацікавилися покращенням FocusQuest. Оскільки це відкритий проєкт, кожен може долучитися до його розвитку: додати нові RPG-механіки, виправити баги або покращити візуал.

Цей короткий гайд допоможе вам швидко розпочати роботу.

## **🗺️ Як зробити внесок (Крок за кроком)**

1. **Зробіть Fork репозиторію:** Натисніть кнопку "Fork" у правому верхньому куті сторінки проєкту на GitHub, щоб створити власну копію репозиторію.  
2. **Клонуйте репозиторій локально:**  
   git clone \[https://github.com/ВАШ\_ЮЗЕРНЕЙМ/FocusQuest.git\](https://github.com/ВАШ\_ЮЗЕРНЕЙМ/FocusQuest.git)  
   cd FocusQuest

3. **Створіть нову гілку (Branch):** Завжди створюйте нову гілку для кожної фічі чи виправлення. Використовуйте зрозумілі назви:  
   git checkout \-b feature/EpicLootSystem  
   \# або для виправлення багів  
   git checkout \-b fix/TimerBug

4. **Внесіть свої зміни:** Пишіть чистий, зрозумілий код. Оскільки проєкт використовує Vanilla JS (без фреймворків), намагайтеся підтримувати наявний стиль та логіку збереження стану (state).  
5. **Закомітьте зміни:** Зробіть зрозумілий опис коміту.  
   git add index.html  
   git commit \-m "Add Epic Loot System mechanics"

6. **Надішліть гілку у свій Fork:**  
   git push origin feature/EpicLootSystem

7. **Відкрийте Pull Request (PR):** Перейдіть до оригінального репозиторію FocusQuest і натисніть "New Pull Request". Опишіть, що саме ви додали чи виправили, і чому це покращить застосунок.

## **🐛 Повідомлення про баги (Bug Reports)**

Якщо ви знайшли помилку, будь ласка, створіть **Issue** в репозиторії.

Вкажіть:

* Вашу операційну систему та браузер.  
* Кроки для відтворення помилки.  
* Що сталося і що мало статися натомість.

## **💡 Пропозиції нових фіч (Feature Requests)**

Ми завжди відкриті до нових ідей\! Загляньте у [ROADMAP.md](https://www.google.com/search?q=./ROADMAP.md), щоб переконатися, що ваша ідея ще не в планах. Якщо її там немає — сміливо відкривайте нове Issue з позначкою enhancement та описуйте свою ідею.

# **🇬🇧 Contributing to FocusQuest (English)**

Welcome to the Developers' Guild\! ⚔️ We are thrilled that you are interested in improving FocusQuest. This is an open-source project, and anyone is welcome to help us add new RPG mechanics, squash bugs, or polish the UI.

## **🗺️ How to Contribute (Step by Step)**

1. **Fork the repository** on GitHub.  
2. **Clone your fork** locally: git clone https://github.com/YOUR\_USERNAME/FocusQuest.git  
3. **Create a feature branch:** git checkout \-b feature/AwesomeNewFeature  
4. **Make your changes** (Please stick to the Vanilla JS style and existing state logic).  
5. **Commit your changes:** git commit \-m "Add Awesome New Feature"  
6. **Push to your fork:** git push origin feature/AwesomeNewFeature  
7. **Open a Pull Request** against the main repository and describe your changes.

If you find bugs or have feature requests, please open an **Issue** on GitHub\!