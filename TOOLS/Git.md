

# Встановлення Git на Windows

Щоб встановити Git на Windows, виконайте наступні кроки:

### 1. **Завантаження Git для Windows**
   - Перейдіть на офіційну сторінку завантаження Git: [https://git-scm.com/download/win](https://git-scm.com/download/win).
   - Завантажиться інсталяційний файл для Windows. Це зазвичай `.exe` файл, наприклад, `Git-2.41.0-64-bit.exe`.

### 2. **Запуск інсталятора**
   - Після завершення завантаження двічі клацніть на файл, щоб запустити інсталятор.
   - Вам буде запропоновано вибір мови. Виберіть **English** або іншу зручну мову для інсталяції.

### 3. **Вибір параметрів інсталяції**
   Під час інсталяції з'являться кілька кроків, де можна вибрати параметри. Ось основні з них:

   - **Choose Components**:
     - Рекомендується залишити параметри за замовчуванням. Включно з опцією **Windows Explorer integration** для зручності використання Git через контекстне меню у провіднику Windows.

   - **Select Start Menu Folder**:
     - Це не має значення для більшості користувачів, тому просто натискайте **Next**.

   - **Choosing the default editor used by Git**:
     - За замовчуванням Git використовує **Vim** як редактор тексту. Якщо ви не звикли до Vim, ви можете вибрати інший редактор, наприклад:
       - **Notepad++** (якщо ви його використовуєте),
       - **VSCode** (якщо у вас встановлений Visual Studio Code),
       - **Atom** або інші.

   - **Adjusting your PATH environment**:
     - Тут рекомендується вибрати опцію **Git from the command line and also from 3rd-party software**. Це дозволить вам використовувати Git як у Git Bash, так і через командний рядок Windows (CMD).

   - **Choosing HTTPS transport backend**:
     - Рекомендується залишити **Use the OpenSSL library**.

   - **Configuring the line ending conversions**:
     - За замовчуванням вибрано **Checkout Windows-style, commit Unix-style line endings**. Це найкращий варіант для роботи з Git на Windows.

   - **Configuring the terminal emulator to use with Git Bash**:
     - Рекомендується вибрати **Use MinTTY (the default terminal of MSYS2)**, оскільки він надає кращу підтримку та більше функцій для роботи з Git.

   - **Extra Options**:
     - Залишайте за замовчуванням. Це додаткові параметри для сумісності з деякими програмами.

### 4. **Інсталяція**
   - Після налаштування параметрів натискайте **Install**.
   - Інсталятор почне встановлення Git на вашу систему. Це займе кілька хвилин.

### 5. **Завершення інсталяції**
   - Після завершення інсталяції натискайте **Finish**.
   - Якщо вибрано запуск Git Bash, відкриється Git Bash — командний рядок для роботи з Git.

### 6. **Перевірка установки Git**
   - Після завершення інсталяції перевірте, чи правильно встановлений Git:
     - Відкрийте **Command Prompt** або **Git Bash**.
     - Введіть команду:
       ```bash
       git --version
       ```
     - Якщо установка пройшла успішно, ви побачите версію Git, наприклад:
       ```bash
       git version 2.41.0.windows.1
       ```

### 7. **Конфігурація Git**
   Після встановлення Git можна налаштувати своє ім'я та електронну адресу для комітів:

   - Відкрийте **Git Bash** або **Command Prompt**.
   - Введіть команду для налаштування вашого імені:
     ```bash
     git config --global user.name "Ваше Ім'я"
     ```
   - І команду для налаштування вашої електронної пошти:
     ```bash
     git config --global user.email "your_email@example.com"
     ```

   Це дозволить Git правильно асоціювати ваші коміти з вашими даними.

### 8. **Git GUI (опційно)**
   Після встановлення Git також можна використовувати графічний інтерфейс для роботи з Git:
   - **Git GUI**: Це простий інтерфейс для виконання базових операцій з Git.
   - Ви можете відкрити його через меню "Пуск" або за допомогою команди:
     ```bash
     git gui
     ```

### Підсумок:
Тепер ви маєте повністю встановлений і налаштований Git на вашій Windows-машині. Ви можете використовувати **Git Bash** для командного рядка, **Git GUI** для графічного інтерфейсу або ж **Command Prompt** для доступу до Git через стандартний Windows інтерфейс.


- Scrum with GitHub No Jira Required!, https://www.youtube.com/watch?v=Is9KZFkHmpk
- Creating a Product Backlog of User Stories for Agile Development using GitHub, https://www.youtube.com/watch?v=m8ZxTHSKSKE


---------------------------------------------------------------------------------------------------------------------------------------------------

- A Beginner’s Guide : GitHub, https://medium.com/@morepravin1989/a-beginners-guide-github-6473051f4a61
- The Ultimate Guide to Git Branching Strategies, https://medium.com/@prateekjain.dev/the-ultimate-guide-to-git-branching-strategies-6324f1aceac2
- Basic Beginner Guide - GitHub CLI, https://medium.com/@morepravin1989/basic-beginner-guide-github-cli-c8a3b16eb3df

- Git fundamentals: A comprehensive guide to effective version control, https://medium.com/@orestis.meikopoulos/git-fundamentals-an-introductory-guide-to-effective-version-control-1ab81cceb5a9
- GitHub Actions for Beginners: Build Your First CI/CD Workflow, https://medium.com/@morepravin1989/github-actions-for-beginners-build-your-first-ci-cd-workflow-489fa0baa861
- GitHub Actions: Your First Workflow (Basic — step by step), https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse2025/tree/main
- GitHub Actions: Hello World for Beginners (For Simple Start), https://medium.com/@morepravin1989/github-actions-hello-world-for-beginners-for-simple-start-e2047d5cd263
- Git vs GitHub vs GitHub Actions — A Beginner-Friendly Guide, https://medium.com/@morepravin1989/git-vs-github-vs-github-actions-a-beginner-friendly-guide-8f4f583c0a81
- 




