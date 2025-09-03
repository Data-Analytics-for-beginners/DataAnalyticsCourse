


# Організація робочого середовища Python з використанням віртуальних середовищ

## Розуміння віртуальних середовищ

Віртуальне середовище, або virtualenv, — це інструмент, який створює ізольований простір для виконання Python. Воно містить власну інсталяцію Python, а також усі необхідні пакети для конкретного проєкту. Це дозволяє мати різні версії Python та пакетів у кожному віртуальному середовищі без взаємного втручання між ними. Така ізоляція є життєво важливою для ефективного управління залежностями кількох проєктів, що дозволяє тестувати нові пакети чи версії пакетів у контрольованому середовищі без ризику для інших проєктів або глобальної системи.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/python_1.webp)


### Навіщо використовувати віртуальні середовища?
- **Ізоляція**: Зберігає залежності кожного проєкту окремо, уникаючи конфліктів.
- **Організація**: Полегшує організацію середовища розробки, особливо в командах.
- **Гнучкість**: Дозволяє тестувати різні версії пакетів без ризику для інших проєктів.

## Налаштування середовища розробки Python з VS Code

Visual Studio Code (VS Code) — це потужний редактор вихідного коду, який підтримує Python серед багатьох інших мов. Налаштування середовища розробки Python у VS Code може значно підвищити вашу продуктивність. Розглянемо як це зробити:

### Крок 1: Встановлення Python

Переконайтеся, що Python встановлено на вашій системі. Якщо його не встановлено, ви можете завантажити останню версію з офіційного веб-сайту Python. Під час встановлення відмітьте опцію додавання Python до системного PATH, що полегшує запуск Python з терміналу.

Інший метод — завантажити безпосередньо з Microsoft потрібну вам версію, яка автоматично виконає всі конфігурації PATH.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/python_2.webp)

Більшість сучасних дистрибутивів GNU/Linux постачаються з попередньо встановленим Python як частиною операційної системи. Щоб перевірити наявність та розташування стандартної інсталяції Python, можна використати таку команду в терміналі:

```
which python3
/usr/bin/python3
```

Цей шлях вказує, де розташований виконуваний файл Python за замовчуванням в операційній системі.

У випадку дистрибутиву Linux Ubuntu 22.04.2 LTS, версія Python, що постачається з системою, — 3.10. Ви можете підтвердити конкретну версію встановленого Python, виконавши команду:

```
python3 --version
```

Це має повернути щось на зразок:

```
Python 3.10.6
```

Це показує версію Python, яка наразі активна та готова до використання в системі.

### Крок 2: Встановлення VS Code

Переконайтеся, що Visual Studio Code вже встановлено на вашій системі; якщо ви ще цього не зробили, ви можете безкоштовно завантажити його з офіційного веб-сайту Visual Studio Code. Дотримуйтесь інструкцій з встановлення, специфічних для вашої операційної системи (Windows, macOS або Linux).

Інший метод — також завантажити з Microsoft Store.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/python_3.webp)

### Крок 3: Встановлення розширення Python у VS Code

Коли VS Code та Python вже встановлені, наступним кроком є встановлення розширення Python для VS Code. Це розширення пропонує потужні функції, такі як автодоповнення коду, лінтинг, налагодження та підтримку віртуальних середовищ. Для встановлення:

1. Відкрийте VS Code.
2. Перейдіть до значка розширень на бічній панелі або натисніть Ctrl+Shift+X.
3. Знайдіть "Python" і шукайте розширення, опубліковане Microsoft.
4. Натисніть "Встановити", щоб додати розширення до вашого VS Code.
   
   ![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/python_4.webp)
   
6. Знайдіть "Jupyter" і шукайте розширення, опубліковане Microsoft.
7. Натисніть "Встановити", щоб додати розширення до вашого VS Code.
   ![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/python_5.webp)

### Крок 4: Встановлення бібліотеки Virtualenv та налаштування віртуальних середовищ

Перш ніж налаштовувати віртуальне середовище у VS Code, вам потрібно мати встановлений virtualenv у вашій системі. Якщо його ще немає, виконайте ці кроки для встановлення:

1. Відкрийте термінал вашої системи.
2. Введіть таку команду для встановлення virtualenv через pip або pip3, менеджер пакетів Python:

```
pip install virtualenv
```

Ці команди завантажують і встановлюють останню версію virtualenv, дозволяючи створювати ізольовані віртуальні середовища для ваших проєктів. У деяких випадках, якщо команда pip не розпізнається, хоча команда python розпізнається, можливо, вам потрібно виконати таку команду:

```
python -m pip install --upgrade pip
```

У Windows також необхідно використовувати virtualenvwrapper, який є набором розширень для інструменту virtualenv, розроблених для оптимізації управління віртуальними середовищами Python. Ці розширення полегшують створення та видалення віртуальних середовищ, а також покращують робочий процес розробки в середовищі Windows.

1. Відкрийте термінал.
2. Встановіть virtualenvwrapper-win: використовуйте pip, менеджер пакетів Python, для встановлення virtualenvwrapper-win. Введіть таку команду:

```
pip install virtualenvwrapper-win
```

**Переваги virtualenvwrapper-win:**
- Спрощене створення та видалення середовищ: Спрощені команди для створення та видалення віртуальних середовищ.
- Краще управління середовищами: Полегшує перемикання між різними віртуальними середовищами та управління їхніми залежностями.
- Покращена організація: Зберігає всі ваші віртуальні середовища в одному місці, уникаючи розкидання по всій системі.

**На цьому етапі...**
У нас будуть встановлені основні ресурси:
- Python
- Visual Studio Code
- Розширення
- Бібліотеки для управління середовищем, такі як virtualenv та wrapper у випадку Windows.

  ![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/python_6.webp)

## Організація робочого простору та управління віртуальними середовищами

Організація робочого простору є важливою для успіху та ефективності в розробці програмного забезпечення. У контексті програмування на Python це включає правильне управління віртуальними середовищами, які є вирішальними для підтримки сумісності та незалежності залежностей кожного проєкту. Цікава стратегія полягає у створенні двох окремих папок: одна для зберігання каталогів проєктів, а інша виключно для virtualenvs. Цей підхід не лише допомагає підтримувати порядок, але й полегшує управління кількома середовищами та проєктами чітко та окремо.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/python_7.webp)

### Важливість організації

Фізичне розділення каталогів проєктів та їхніх відповідних virtualenvs має кілька переваг:

- **Ясність**: Полегшує розуміння того, які віртуальні середовища пов'язані з кожним проєктом.
- **Обслуговування**: Спрощує процес оновлення або видалення віртуального середовища без прямого впливу на файли проєкту.
- **Резервне копіювання та міграція**: Це робить більш практичним резервне копіювання або міграцію проєктів та віртуальних середовищ, які можна виконувати незалежно.

### Практичний підхід!

Щоб реалізувати цю стратегію у вашому середовищі розробки Python, спочатку створіть віртуальне середовище в каталозі, присвяченому virtualenvs. Виконайте ці кроки в інтегрованому терміналі вашого редактора коду або системному терміналі:

1. Відкрийте PowerShell як адміністратор на Windows.
2. Перейдіть до папки virtualenvs, наприклад:
```
cd C:\ваш\шлях\до\папки\venvs
```
3. Виконайте команду для створення нового virtualenv, замінивши environment_name бажаною назвою для віртуального середовища:

На Windows:
```
python -m venv environment_name
```

На Unix або macOS:
```
python3 -m venv environment_name
```

4. Щоб активувати новостворене віртуальне середовище:

На Windows:
```
environment_name\Scripts\activate
```

На Unix або macOS:
```
source environment_name/bin/activate
```

Якщо в терміналі нічого не з'являється, не хвилюйтеся. Ви можете відкрити папку venvs і перевірити, чи воно там є.

5. Використання env у VS Code:

- Відкрийте Visual Studio Code.
- Натисніть Ctrl+Shift+P.
- Знайдіть опцію Python: Select interpreter.
- Якщо virtualenv не з'являється, як показано нижче...
- Натисніть Enter interpreter path.
- Натисніть find... і перейдіть до папки Scripts віртуального середовища, виберіть Python.
- Натисніть Select Interpreter.

Тепер воно з'явиться у списку для використання.

З цього моменту ми можемо створити код Python або Jupyter Notebook і запустити його з нашим створеним середовищем:

**Код Python**

Виберіть потрібне середовище з верхнього правого кута VS Code під час редагування .py файлу.

**Код Jupyter**

Виберіть бажаний ipykernel (env).

Якщо у вас ще немає ядра Jupyter Notebook, просто прийміть це, і VS Code виконає необхідні конфігурації в env.

Нарешті, виконання буде успішним.

## Висновок

Організація вашого середовища для вивчення Python з віртуальними середовищами спочатку може здаватися складною, але це фундаментальна навичка для ефективної розробки проєктів. Вона дозволяє безпечно експериментувати з різними версіями пакетів і підтримує вашу систему чистою та організованою. Правильне налаштування середовища розробки з VS Code та віртуальними середовищами дає вам потужну основу для ваших проєктів на Python.





1) How to Organize Your Python Study Environment with Virtual Environments: A Complete Guide, https://medium.com/@lucasmassucci/how-to-organize-your-python-study-environment-with-virtual-environments-a-complete-guide-d388a26afa9e
2) I Tried Writing Python in VS Code and PyCharm — Here’s What I Found, https://medium.com/pythonic-af/i-tried-writing-python-in-vs-code-and-pycharm-heres-what-i-found-e041becf6900
3) VS Code’s New AI Did My Job for 30 Minutes. The Results? Honestly Shocking!, https://medium.com/mr-plan-publication/vs-codes-new-ai-did-my-job-for-30-minutes-the-results-honestly-shocking-33b490a5afde
4) 





- Mastering Python Project Management with uv Part 1: It’s Time to Ditch Poetry!, https://bury-thomas.medium.com/mastering-python-project-management-with-uv-part1-its-time-to-ditch-poetry-c2590091d90a
- Mastering Python Project Management with uv: Part 2 — Deep Dives and Advanced Use, https://bury-thomas.medium.com/mastering-python-project-management-with-uv-part-2-deep-dives-and-advanced-use-1e2540e6f4a6
- Mastering Python Project Management with uv: Part 5 — advanced CI/CD Nox and uv.cli, https://bury-thomas.medium.com/mastering-python-project-management-with-uv-part-5-advanced-ci-cd-nox-and-uv-cli-da855782af3f
- uv Package Manager for Python, https://medium.com/@nimritakoul01/uv-package-manager-for-python-f92c5a760a1c
- Build and Publish a Python Package with uv, https://medium.com/@shouke.wei/build-and-publish-a-python-package-with-uv-50a5225616c4
- Using UV and Conda Together Effectively: A Fast, Flexible Workflow, https://medium.com/@datagumshoe/using-uv-and-conda-together-effectively-a-fast-flexible-workflow-d046aff622f0
- Python UV + pyproject.toml: The Fastest Way to Run Python Apps, https://medium.com/@philip.mutua/python-uv-pyproject-toml-the-fastest-way-to-run-python-apps-913d6213c111
- Python: Monorepo with UV, https://medium.com/@life-is-short-so-enjoy-it/python-monorepo-with-uv-f4ced6f1f425
- How to Structure Python Projects Like a Professional Engineer, https://thepythonworld.in/how-to-structure-python-projects-like-a-professional-engineer-210a949834cb
- Python 3.14, https://python.plainenglish.io/python-3-14-e7ab21757418
- Mastering AI Automation with Python and Modern Tools, https://python.plainenglish.io/mastering-ai-automation-with-python-and-modern-tools-b208221606fb
- The Python Automation System That Quietly Earns Me Money Every Month, https://python.plainenglish.io/the-python-automation-system-that-quietly-earns-me-money-every-month-1b5ce5280efa
- 
