# **⚔️ FocusQuest**

**FocusQuest** — це гейміфікований трекер завдань та часу, розроблений спеціально для підтримки продуктивності, утримання фокусу та боротьби з прокрастинацією (створений з урахуванням особливостей РДУГ / ADHD-friendly).

Перетворіть свою щоденну рутину на епічну RPG-пригоду, де ви — головний герой, що заробляє золото, здобуває досвід та долає босів (ваші дедлайни)\!

## **✨ Головні фічі**

* 🎮 **Класи та RPG-механіки:** Обирайте свій шлях (Воїн, Маг або Розбійник) з унікальними пасивними бонусами. Заробляйте досвід (XP) та підвищуйте рівень. Бережіть здоров'я (HP) — воно падає за прокрастинацію.  
* ⏱️ **Анти-відволікаючий таймер:** Трекайте час для кожної задачі чи підзадачі. Зупинили таймер раніше ніж за 5 хвилин? Отримайте штраф (шкоду) за відволікання\! Можливість вносити час вручну та скасовувати випадкові сесії.  
* 🎯 **Оцінка часу (Estimates):** Встановлюйте очікуваний час для задач. Вкладаєтесь у дедлайн? Отримуйте "Критичний удар" із подвійним досвідом та золотом\!  
* 🏆 **Досягнення (Achievements):** Виконуйте специфічні умови (наприклад, фокус понад годину без перерв), щоб розблокувати унікальні бейджі та отримати цінні нагороди.  
* 💰 **Економіка та Крамниця:** Встановлюйте погодинну ставку (rate) для проєктів, рахуйте реальний прибуток. Витрачайте ігрове золото на Зілля Здоров'я чи Фокусу.  
* 🐉 **Битви з Босами:** Перетворіть складний проєкт на "Боса" з власною смугою здоров'я, яка зменшується з кожним виконаним кроком.  
* ☁️ **Google Авторизація та Хмара:** Входьте в один клік через Google. Ваш прогрес безпечно синхронізується між усіма пристроями через Firebase. Конфлікти синхронізації між локальними даними та хмарою вирішуються зручним діалоговим вікном.  
* 📱 **PWA та Мультимедіа:** Встановлюйте як нативний додаток на телефон. Насолоджуйтесь 8-бітними звуками, фоновими патернами та темною/світлою темами.

## **🛠 Технології**

Проєкт максимально легкий і працює повністю в браузері.

* **HTML5 / CSS3** (Включно з CSS Mask для фонових патернів)  
* **JavaScript (Vanilla/ES6)** (Без важких фреймворків)  
* **Tailwind CSS** (Стилізація)  
* **FontAwesome** (Іконки)  
* **Firebase Auth & Firestore** (Авторизація та БД)

## **🚀 Як почати користуватися (Встановлення)**

### **Варіант 1: Локальне використання (Offline)**

Просто завантажте код, відкрийте index.html у браузері та користуйтеся\! Усі дані автоматично зберігатимуться в localStorage вашого браузера.

### **Варіант 2: Власний хостинг із Хмарною Синхронізацією (Vercel \+ Firebase)**

Щоб увімкнути збереження в хмарі та авторизацію через Google без розкриття ваших ключів:

1. Створіть проєкт у [Firebase Console](https://www.google.com/search?q=https://console.firebase.google.com/), увімкніть **Firestore** та **Google Authentication**.  
2. Встановіть правила безпеки Firestore (щоб кожен читав лише свої дані):  
   rules\_version \= '2';  
   service cloud.firestore {  
     match /databases/{database}/documents {  
       match /focusquest\_users/{userId} {  
         allow read, write: if request.auth \!= null && request.auth.uid \== userId;  
       }  
     }  
   }

3. Створіть файл env.js у корені проєкту (і додайте його в .gitignore\!). Вставте туди ваші ключі:  
   const firebaseConfig \= {  
       apiKey: "ВАШ\_API\_KEY",  
       authDomain: "ВАШ\_PROJECT.firebaseapp.com",  
       projectId: "ВАШ\_PROJECT\_ID"  
   };

4. Підключіть env.js у секції \<head\> вашого index.html: \<script src="env.js"\>\</script\>. Знайдіть об'єкт firebaseConfig в index.html і видаліть або закоментуйте його, щоб він брався з env.js.  
5. **Деплой на Vercel:** У налаштуваннях проєкту на Vercel додайте змінні середовища (FIREBASE\_API\_KEY, FIREBASE\_AUTH\_DOMAIN, FIREBASE\_PROJECT\_ID). У Build Command впишіть:  
   echo "const firebaseConfig \= { apiKey: '$FIREBASE\_API\_KEY', authDomain: '$FIREBASE\_AUTH\_DOMAIN', projectId: '$FIREBASE\_PROJECT\_ID' };" \> env.js

## **🗺️ Плани, Історія та Внесок**

Ми постійно розвиваємо FocusQuest\! Загляньте у ці файли, щоб дізнатися більше про екосистему проєкту:

* 📍 [**ROADMAP.md**](https://www.google.com/search?q=./ROADMAP.md) — наші плани на майбутні оновлення, нові механіки та ідеї з беклогу.  
* 📜 [**CHANGELOG.md**](https://www.google.com/search?q=./CHANGELOG.md) — детальна історія всіх випущених оновлень та реалізованих фіч.  
* 🤝 [**CONTRIBUTING.md**](https://www.google.com/search?q=./CONTRIBUTING.md) — гайд для розробників. Дізнайтеся, як приєднатися до Гільдії та допомогти нам з кодом\!

## **📄 Ліцензія**

Цей проєкт розповсюджується на умовах ліцензії MIT. Детальніше див. у файлі [LICENSE](https://www.google.com/search?q=./LICENSE).

*Створено з ❤️ та за допомогою магії Google Gemini для продуктивності без вигорання.*

# **🇬🇧 FocusQuest (English)**

**FocusQuest** is a gamified task and time tracker designed specifically to boost productivity, maintain focus, and fight procrastination (ADHD-friendly).

Turn your daily routine into an epic RPG adventure where you are the main hero, earning gold, gaining experience, and defeating bosses (your deadlines)\!

## **✨ Key Features**

* 🎮 **Classes & RPG Mechanics:** Choose your path (Warrior, Mage, or Rogue) with unique passive buffs. Earn XP to level up. Protect your health (HP)—it drops when you procrastinate.  
* ⏱️ **Anti-distraction Timer:** Track time for each quest or subtask. Stopped the timer in under 5 minutes? Take damage (HP penalty) for getting distracted\! Support for manual time entry and discarding accidental sessions.  
* 🎯 **Time Estimates:** Set estimated times for your tasks. Beat the deadline? Land a "Critical Hit" for double XP and extra gold\!  
* 🏆 **Achievements:** Complete specific challenges (e.g., focus for 60+ mins without a break) to unlock unique badges and claim valuable rewards.  
* 💰 **Economy & Guild Shop:** Set an hourly rate for projects to track real-world earnings. Spend your in-game gold on Health or Focus Potions.  
* 🐉 **Boss Battles:** Turn a complex project into a "Boss" with its own health bar that depletes as you complete its tasks.  
* ☁️ **Google Auth & Cloud Sync:** Log in with one click via Google. Your progress securely syncs across all your devices via Firebase. Smart conflict resolution popups are included.  
* 📱 **PWA & Multimedia:** Install it as a native app on your phone. Enjoy 8-bit sound effects, seamless background patterns, and Dark/Light themes.

## **🛠 Tech Stack**

The project is extremely lightweight and runs entirely in the browser.

* **HTML5 / CSS3** (Including CSS Masks for background patterns)  
* **JavaScript (Vanilla/ES6)** (No heavy frameworks)  
* **Tailwind CSS** (Styling)  
* **FontAwesome** (Icons)  
* **Firebase Auth & Firestore** (Authentication and Database)

## **🚀 Getting Started (Installation)**

### **Option 1: Local Usage (Offline)**

Simply download the code, open index.html in your browser, and start your journey\! All data is automatically saved to your browser's localStorage.

### **Option 2: Self-Hosting with Cloud Sync (Vercel \+ Firebase)**

To enable cloud saving and Google Auth without exposing your API keys:

1. Create a project in the [Firebase Console](https://www.google.com/search?q=https://console.firebase.google.com/), enable **Firestore** and **Google Authentication**.  
2. Set up Firestore Security Rules (so users can only read/write their own data):  
   rules\_version \= '2';  
   service cloud.firestore {  
     match /databases/{database}/documents {  
       match /focusquest\_users/{userId} {  
         allow read, write: if request.auth \!= null && request.auth.uid \== userId;  
       }  
     }  
   }

3. Create an env.js file in the root of the project (and add it to your .gitignore\!). Insert your keys:  
   const firebaseConfig \= {  
       apiKey: "YOUR\_API\_KEY",  
       authDomain: "YOUR\_PROJECT.firebaseapp.com",  
       projectId: "YOUR\_PROJECT\_ID"  
   };

4. Include env.js in the \<head\> of your index.html: \<script src="env.js"\>\</script\>. Make sure to remove or comment out the hardcoded firebaseConfig object inside index.html.  
5. **Deploying on Vercel:** In your Vercel project settings, add the Environment Variables (FIREBASE\_API\_KEY, FIREBASE\_AUTH\_DOMAIN, FIREBASE\_PROJECT\_ID). Set the Build Command to:  
   echo "const firebaseConfig \= { apiKey: '$FIREBASE\_API\_KEY', authDomain: '$FIREBASE\_AUTH\_DOMAIN', projectId: '$FIREBASE\_PROJECT\_ID' };" \> env.js

## **🗺️ Roadmap, Changelog & Contributing**

We are constantly improving FocusQuest\! Check out these files to learn more about the project's ecosystem:

* 📍 [**ROADMAP.md**](https://www.google.com/search?q=./ROADMAP.md) — Our plans for future updates, new mechanics, and backlog ideas.  
* 📜 [**CHANGELOG.md**](https://www.google.com/search?q=./CHANGELOG.md) — A detailed history of all released updates and features.  
* 🤝 [**CONTRIBUTING.md**](https://www.google.com/search?q=./CONTRIBUTING.md) — A guide for developers. Learn how to join the Guild and help us build new features\!

## **📄 License**

This project is licensed under the MIT License. See the [LICENSE](https://www.google.com/search?q=./LICENSE) file for details.