
# 1 Що таке SQL Server

SQL Server — це система управління реляційними базами даних (РСУБД), розроблена та випущена на ринок компанією Microsoft.

Подібно до інших програмних РСУБД, SQL Server побудований на основі SQL, стандартної мови програмування для взаємодії з реляційними базами даних. SQL Server пов'язаний з Transact-SQL, або T-SQL, реалізацією SQL від Microsoft, яка включає набір власних програмних конструкцій.

SQL Server протягом понад 20 років був доступний виключно для середовища Windows. У 2016 році Microsoft зробила його доступним для Linux. SQL Server 2017 став загальнодоступним у жовтні 2016 року і був сумісний як з Windows, так і з Linux.

## Архітектура SQL Server

На наступній схемі показана архітектура SQL Server:

![Архітектура SQL Server](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/sql-server-architecture.png)


SQL Server складається з двох основних компонентів:
* Ядро бази даних (Database Engine)
* SQLOS

### Ядро бази даних

Основним компонентом SQL Server є ядро бази даних, яке складається з реляційного ядра, що обробляє запити, та ядра зберігання, яке керує файлами бази даних, сторінками, індексами тощо.

Крім того, ядро бази даних створює об'єкти бази даних, такі як збережені процедури, представлення та тригери.

### Реляційне ядро

Реляційне ядро містить компоненти, які визначають оптимальний метод виконання запиту. Його також називають процесором запитів.

Реляційне ядро запитує дані з ядра зберігання на основі вхідного запиту та обробляє результати.

Деякими завданнями реляційного ядра є обробка запитів, управління пам'яттю, управління потоками та завданнями, управління буфером та розподілена обробка запитів.

### Ядро зберігання

Ядро зберігання відповідає за зберігання та отримання даних із систем зберігання, таких як диски та SAN.

### SQLOS

Під реляційним ядром та ядром зберігання знаходиться операційна система SQL Server, або SQLOS.

SQLOS надає різноманітні послуги операційної системи, такі як управління пам'яттю та вводом-виводом, а також обробку винятків та сервіси синхронізації.

## Сервіси та інструменти SQL Server

Microsoft пропонує як інструменти та сервіси управління даними, так і бізнес-аналітики (BI) разом із SQL Server.

Для управління даними SQL Server включає SQL Server Integration Services (SSIS), SQL Server Data Quality Service та SQL Server Master Data Services.

Для розробки баз даних SQL Server надає SQL Server Data Tools; а для управління, розгортання та моніторингу баз даних SQL Server має SQL Server Management Studio (SSMS).

Для аналізу даних SQL Server пропонує SQL Server Analysis Services (SSAS). SQL Server Reporting Services (SSRS) надає звіти та візуалізацію даних. Технологія Machine Learning Services вперше з'явилася в SQL Server 2016, початково відома як R Services.

## Редакції SQL Server

SQL Server має чотири основні редакції, кожна з яких пропонує різні пакетні сервіси та інструменти. Дві редакції доступні безкоштовно:

**SQL Server Developer Edition** призначена для розробки та тестування баз даних.

**SQL Server Express Edition** підходить для невеликих баз даних з обсягом зберігання до 10 ГБ.

Для більших та критичніших застосунків SQL Server пропонує **редакцію Enterprise**, яка включає всі функції SQL Server.

**SQL Server Standard Edition** має підмножину функцій, доступних у редакції Enterprise, та накладає обмеження на сервер, включаючи обмеження на кількість ядер процесора та конфігурації пам'яті.

**SQL Server Web Edition** є хорошим варіантом для компаній, що займаються веб-хостингом, завдяки низькій загальній вартості володіння.

Для детальної інформації про редакції SQL Server перегляньте доступні редакції Server Server 2022.

## Підсумок

* Архітектура SQL server включає ядро бази даних та операційну систему SQL server (SQLOS)
* SQL server пропонує набір інструментів для ефективної роботи з даними
* SQL server має різні редакції, включаючи редакцію для розробників, Express, Enterprise та Standard

# 2 Встановлення SQL Server

**Резюме**: у цьому навчальному посібнику ви дізнаєтеся, як встановити SQL Server 2022 Developer Edition та SQL Server Management Studio (SSMS).

## Встановлення SQL Server 2022 Developer Edition

### Завантаження SQL Server 2022

Щоб завантажити SQL Server 2022, натисніть на посилання нижче:
[Завантажити SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)

Microsoft пропонує кілька редакцій SQL Server. Для навчальних цілей ви можете завантажити редакцію Developer.

**Крок 1.** Завантажувач запитає вас вибрати тип встановлення. Виберіть опцію **Download Media**, яка дозволяє спочатку завантажити файли налаштування, а потім встановити SQL Server:
![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/Download-SQL-Server-Installer-1.png)

**Крок 2.** Виберіть папку для зберігання файлів встановлення, а потім натисніть кнопку **Download**:
![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/Download-SQL-Server-Installer-2.png)

**Крок 3.** Завантажувач почне завантажувати файли встановлення. Цей процес може зайняти кілька хвилин, залежно від швидкості вашого інтернет-з'єднання.
![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/Download-SQL-Server-Installer-3.png)

**Крок 4.** Після завершення завантаження відкрийте папку, де зберігається завантажений файл:

**Крок 5.** Відкрийте файл **SQLServer2022-DEV-x64-ENU**, щоб запустити встановлення. Він розпакує файли в каталог і розпочне процес встановлення.

### Встановлення SQL Server 2022 Developer Edition

**Крок 1.** Після запуску інсталятора з'явиться вікно SQL Server Installation Center; виберіть опцію **Installation** ліворуч:

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/1-Install-SQL-Server-Server-Installation-Center.png)

**Крок 2.** Виберіть редакцію Developer для встановлення та натисніть кнопку Next:

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/2-SQL-Server-2022-Setup.png)

**Крок 3.** Позначте "I accept the license terms." та натисніть кнопку Next:
![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/3-SQL-Server-2022-Setup.png)

**Крок 4.** Якщо ви не хочете отримувати оновлення для SQL Server, зніміть позначку "Use Microsoft Update to check for updates (recommended)" та натисніть кнопку **Next**:

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/4-SQL-Server-2022-Setup.png)


**Крок 5.** Встановлення перевірить передумови перед продовженням. Якщо помилок немає, натисніть кнопку Next:

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/5-SQL-Server-2022-Setup.png)

**Крок 6.** Зніміть позначку з Azure extension for SQL Server:

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/6-SQL-Server-2022-Setup.png)

**Крок 7.** Виберіть функції, які ви хочете встановити. Для навчальних цілей вам потрібні Database Engine Services, натисніть кнопку Next, щоб продовжити:

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/7-SQL-Server-2022-Setup.png)

**Крок 8.** Введіть ID екземпляра SQL Server і натисніть кнопку Next. ID екземпляра за замовчуванням `MSSQLServer`:
![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/8-SQL-Server-2022-Setup.png)

**Крок 9.** Вкажіть облікові записи служб та конфігурацію сортування. Використовуйте налаштування за замовчуванням та натисніть кнопку Next:

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/9-SQL-Server-2022-Setup.png)

**Крок 10.** Вкажіть режим безпеки автентифікації ядра бази даних. Виберіть **Mixed Mode** (1) і введіть пароль для облікового запису системного адміністратора (`sa`) (2 і 3), та додайте поточного користувача як адміністратора SQL Server (4):

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/10-SQL-Server-2022-Setup.png)

Обов'язково зберігайте цей пароль у безпечному місці, оскільки він знадобиться вам для підключення до SQL Server пізніше.

**Крок 11.** Переконайтеся, що функції SQL Server 2022 встановлені.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/11-SQL-Server-2022-Setup.png)


**Крок 12.** Натисніть кнопку **Close**, щоб завершити встановлення.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/12-SQL-Server-2022-Setup.png)

Вітаємо! Ви успішно встановили SQL Server 2022 Developer Edition.

## Microsoft SQL Server Management Studio (SSMS)

Для взаємодії з SQL Server ви можете використовувати інструмент SQL Server клієнта, такий як SQL Server Management Studio (SSMS), наданий Microsoft.

SQL Server Management Studio — це програмне забезпечення для запитів, проектування та управління SQL Server на вашому локальному комп'ютері, віддаленому сервері або в хмарі. Воно надає вам інструменти для налаштування, моніторингу та адміністрування екземплярів SQL Server.

### Завантаження SQL Server Management Studio

По-перше, завантажте SSMS з веб-сайту Microsoft за наступним посиланням:
[Завантажити](https://learn.microsoft.com/en-us/ssms/download-sql-server-management-studio-ssms)  SQL Server Management Studio

По-друге, двічі клацніть файл встановлення **SSMS-Setup-ENU.exe**, щоб запустити інсталятор. Процес встановлення SMSS простий. Вам потрібно слідувати послідовності екранів.

### Встановлення SQL Server Management Studio

**Крок 1.** Натисніть кнопку **Install**:

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/Install-SSMS-1.png)

**Крок 2.** Зачекайте кілька хвилин, поки інсталятор налаштовує програмне забезпечення:
![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/Install-SSMS-2.png)

**Крок 3.** Після завершення налаштування натисніть кнопку **Close**:
![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/Install-SSMS-3.png)

Тепер у вас повинні бути встановлені SQL Server 2022 та SQL Server Management Studio на вашому комп'ютері. Далі ви дізнаєтеся, як підключитися до SQL Server з SQL Server Management Studio.

   


# 3 Підключення до SQL Server

## Резюме
У цьому розділі лекції ви дізнаєтеся, як підключитися до SQL Server за допомогою SQL Server Management Studio та виконати запит.

## Підключення до SQL Server за допомогою SSMS

Щоб підключитися до SQL Server за допомогою Microsoft SQL Server Management Studio, виконайте наступні кроки:

### Крок 1. Запустіть Microsoft SQL Server Management Studio

Знайдіть програму у меню "Пуск" або на робочому столі та запустіть її.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/SSMS-connect-to-SQL-Server.png)


### Крок 2. Виберіть **Database Engine** з меню **Connect** у розділі **Object Explorer**

При запуску SSMS відкриється вікно підключення. Якщо воно не відкрилося автоматично, ви можете знайти цю опцію в меню Object Explorer.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/Open-the-Connection-Dialog.png)


### Крок 3. Введіть наступну інформацію для підключення:

1. Тип сервера (Server Type): **Database Engine**
2. Ім'я сервера (Server name): **localhost**
3. Автентифікація (Authentication): **SQL Server Authentication**
4. Логін (Login): **sa**
5. Пароль (Password): (Той, який ви ввели під час встановлення)
6. Позначте опцію **Remember Password** (Запам'ятати пароль)
7. Шифрування (Encryption): **Optional** (Необов'язково)

Натисніть кнопку **Connect** (Підключитися), щоб підключитися до SQL Server.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/Connect-to-Local-Server-Server.png)

Якщо підключення пройшло успішно, ви побачите панель **Object Explorer** з вашим сервером.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/Connect-Microsoft-SQL-Server-Management-Studio.png)

## Виконання запиту

Щоб виконати запит, дотримуйтесь наступних кроків:

### Крок 1. Створення нового запиту
Клацніть правою кнопкою миші на вузлі **localhost (SQL Server ...)** і виберіть пункт меню **New Query** (Новий запит).

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/New-Query.png)

### Крок 2. Введення запиту
Введіть наступний запит у вікні редактора:

```sql
select @@version;
```

Цей запит повертає версію SQL Server.

### Крок 3. Виконання запиту
Натисніть кнопку **Execute** (Виконати) або використайте клавішу **F5** для швидкого виконання.

У вікні **Results** (Результати) буде показана версія вашого SQL Server, як показано на знімку екрана вище.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/SSMS-Execute-a-Query.png)


## Висновок

Тепер ви знаєте, як підключитися до SQL Server та виконати запит за допомогою SQL Server Management Studio. Це базові навички, які дозволять вам працювати з базами даних SQL Server і виконувати різноманітні операції.

В наступних розділах ми розглянемо більш складні запити та операції з базами даних SQL Server.



# 4 Зразкова база даних SQL Server: BikeStores

У цьому розділі ви дізнаєтеся про зразкову базу даних SQL Server під назвою BikeStores.

## Структура бази даних

На діаграмі нижче зображена структура бази даних BikeStores:

![Діаграма бази даних BikeStores](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/SQL-Server-Sample-Database.png)


Як бачите з діаграми, зразкова база даних BikeStores має дві схеми: `sales` (продажі) та `production` (виробництво), які містять дев'ять таблиць.

## Таблиці бази даних

### Таблиця sales.stores
Таблиця `sales.stores` містить інформацію про магазини. Кожен магазин має назву, контактну інформацію, таку як телефон та електронна пошта, а також адресу, що включає вулицю, місто, штат та поштовий індекс.

```sql
CREATE TABLE sales.stores (
	store_id INT IDENTITY (1, 1) PRIMARY KEY,
	store_name VARCHAR (255) NOT NULL,
	phone VARCHAR (25),
	email VARCHAR (255),
	street VARCHAR (255),
	city VARCHAR (255),
	state VARCHAR (10),
	zip_code VARCHAR (5)
);
```

### Таблиця sales.staffs
Таблиця `sales.staffs` зберігає основну інформацію про співробітників, включаючи ім'я та прізвище. Вона також містить контактну інформацію, таку як електронна пошта та телефон.

Співробітник працює в магазині, визначеному значенням у стовпці `store_id`. У магазині може працювати один або кілька співробітників.

Співробітник звітує менеджеру магазину, визначеному значенням у стовпці `manager_id`. Якщо значення в `manager_id` є null, то цей співробітник є головним менеджером.

Якщо співробітник більше не працює в жодному магазині, значення в стовпці `active` встановлюється на нуль.

```sql
CREATE TABLE sales.staffs (
	staff_id INT IDENTITY (1, 1) PRIMARY KEY,
	first_name VARCHAR (50) NOT NULL,
	last_name VARCHAR (50) NOT NULL,
	email VARCHAR (255) NOT NULL UNIQUE,
	phone VARCHAR (25),
	active tinyint NOT NULL,
	store_id INT NOT NULL,
	manager_id INT,
	FOREIGN KEY (store_id) 
        REFERENCES sales.stores (store_id) 
        ON DELETE CASCADE ON UPDATE CASCADE,
	FOREIGN KEY (manager_id) 
        REFERENCES sales.staffs (staff_id) 
        ON DELETE NO ACTION ON UPDATE NO ACTION
);
```

### Таблиця production.categories
Таблиця `production.categories` зберігає категорії велосипедів, такі як дитячі велосипеди, комфортні велосипеди та електровелосипеди.

```sql
CREATE TABLE production.categories (
	category_id INT IDENTITY (1, 1) PRIMARY KEY,
	category_name VARCHAR (255) NOT NULL
);
```

### Таблиця production.brands
Таблиця `production.brands` зберігає інформацію про бренди велосипедів, наприклад, Electra, Haro та Heller.

```sql
CREATE TABLE production.brands (
	brand_id INT IDENTITY (1, 1) PRIMARY KEY,
	brand_name VARCHAR (255) NOT NULL
);
```

### Таблиця production.products
Таблиця `production.products` зберігає інформацію про продукти, таку як назва, бренд, категорія, рік моделі та прейскурантна ціна.

Кожен продукт належить до бренду, визначеного стовпцем `brand_id`. Отже, бренд може мати нуль або багато продуктів.

Кожен продукт також належить до категорії, визначеної стовпцем `category_id`. Також кожна категорія може мати нуль або багато продуктів.

```sql
CREATE TABLE production.products (
	product_id INT IDENTITY (1, 1) PRIMARY KEY,
	product_name VARCHAR (255) NOT NULL,
	brand_id INT NOT NULL,
	category_id INT NOT NULL,
	model_year SMALLINT NOT NULL,
	list_price DECIMAL (10, 2) NOT NULL,
	FOREIGN KEY (category_id) 
        REFERENCES production.categories (category_id) 
        ON DELETE CASCADE ON UPDATE CASCADE,
	FOREIGN KEY (brand_id) 
        REFERENCES production.brands (brand_id) 
        ON DELETE CASCADE ON UPDATE CASCADE
);
```

### Таблиця sales.customers
Таблиця `sales.customers` зберігає інформацію про клієнтів, включаючи ім'я, прізвище, телефон, електронну пошту, вулицю, місто, штат та поштовий індекс.

```sql
CREATE TABLE sales.customers (
	customer_id INT IDENTITY (1, 1) PRIMARY KEY,
	first_name VARCHAR (255) NOT NULL,
	last_name VARCHAR (255) NOT NULL,
	phone VARCHAR (25),
	email VARCHAR (255) NOT NULL,
	street VARCHAR (255),
	city VARCHAR (50),
	state VARCHAR (25),
	zip_code VARCHAR (5)
);
```

### Таблиця sales.orders
Таблиця `sales.orders` зберігає інформацію заголовка замовлення на продаж, включаючи клієнта, статус замовлення, дату замовлення, необхідну дату, дату відправлення.

Вона також зберігає інформацію про те, де було створено транзакцію продажу (магазин) і хто її створив (співробітник).

Кожне замовлення на продаж має рядок у таблиці `sales.orders`. Замовлення на продаж має один або кілька рядків елементів, що зберігаються в таблиці `sales.order_items`.

```sql
CREATE TABLE sales.orders (
	order_id INT IDENTITY (1, 1) PRIMARY KEY,
	customer_id INT,
	order_status tinyint NOT NULL,
	-- Order status: 1 = Pending; 2 = Processing; 3 = Rejected; 4 = Completed
	order_date DATE NOT NULL,
	required_date DATE NOT NULL,
	shipped_date DATE,
	store_id INT NOT NULL,
	staff_id INT NOT NULL,
	FOREIGN KEY (customer_id) 
        REFERENCES sales.customers (customer_id) 
        ON DELETE CASCADE ON UPDATE CASCADE,
	FOREIGN KEY (store_id) 
        REFERENCES sales.stores (store_id) 
        ON DELETE CASCADE ON UPDATE CASCADE,
	FOREIGN KEY (staff_id) 
        REFERENCES sales.staffs (staff_id) 
        ON DELETE NO ACTION ON UPDATE NO ACTION
);
```

### Таблиця sales.order_items
Таблиця `sales.order_items` зберігає елементи замовлення на продаж. Кожен елемент належить до замовлення на продаж, визначеного стовпцем `order_id`.

Елемент замовлення на продаж включає продукт, кількість замовлення, прейскурантну ціну та знижку.

```sql
CREATE TABLE sales.order_items(
	order_id INT,
	item_id INT,
	product_id INT NOT NULL,
	quantity INT NOT NULL,
	list_price DECIMAL (10, 2) NOT NULL,
	discount DECIMAL (4, 2) NOT NULL DEFAULT 0,
	PRIMARY KEY (order_id, item_id),
	FOREIGN KEY (order_id) 
        REFERENCES sales.orders (order_id) 
        ON DELETE CASCADE ON UPDATE CASCADE,
	FOREIGN KEY (product_id) 
        REFERENCES production.products (product_id) 
        ON DELETE CASCADE ON UPDATE CASCADE
);
```

### Таблиця production.stocks
Таблиця `production.stocks` зберігає інформацію про запаси, тобто кількість конкретного продукту в певному магазині.

```sql
CREATE TABLE production.stocks (
	store_id INT,
	product_id INT,
	quantity INT,
	PRIMARY KEY (store_id, product_id),
	FOREIGN KEY (store_id) 
        REFERENCES sales.stores (store_id) 
        ON DELETE CASCADE ON UPDATE CASCADE,
	FOREIGN KEY (product_id) 
        REFERENCES production.products (product_id) 
        ON DELETE CASCADE ON UPDATE CASCADE
);
```



# 5 Завантаження зразкової бази даних

У цьому розділі лекції ви дізнаєтеся, як створити нову базу даних у SQL Server та виконати скрипт для завантаження зразкової бази даних.

## Підготовчі кроки

По-перше, вам потрібно завантажити наступний zip-файл, якщо ви ще цього не зробили:
**Завантажити зразкову базу даних SQL Server**

По-друге, розархівуйте zip-файл, і ви побачите три SQL-скрипти:
* `BikeStores Sample Database - create objects.sql` – цей файл призначений для створення об'єктів бази даних, включаючи схеми та таблиці.
* `BikeStores Sample Database - load data.sql` – цей файл призначений для вставки даних у таблиці.
* `BikeStores Sample Database - drop all objects.sql` – цей файл призначений для видалення таблиць та їхніх схем із зразкової бази даних. Він корисний, коли ви хочете оновити зразкову базу даних.

По-третє, давайте створимо базу даних, створимо схеми й таблиці та завантажимо зразкові дані.

## Покроковий процес

### Крок 1
Підключіться до SQL Server, (1) вибравши ім'я сервера, (2) ввівши користувача та (3) пароль і (4) натиснувши кнопку **Підключитися**.
![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/step-1-login-to-the-SQL-Server.png)

### Крок 2
Клацніть правою кнопкою миші на вузлі **Бази даних** у вікні **Оглядач об'єктів** та виберіть пункт меню **Нова база даних...**
![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/step-2-create-a-new-database.png)

### Крок 3
(1) Введіть **Ім'я бази даних** як BikeStores та (2) натисніть кнопку **OK**, щоб створити нову базу даних.
![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/step-3-enter-the-database-information.png)

### Крок 4
Якщо все добре, ви побачите базу даних **BikeStores** під вузлом Бази даних, як показано на знімку екрана нижче:
![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/step-4-new-database-created.png)

### Крок 5
У меню Файл виберіть пункт Відкрити > Файл..., щоб відкрити файл скрипту.
![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/step-5-open-sql-script-file-to-create-objects.png)

### Крок 6
Виберіть файл **BikeStores Sample Database – create objects.sql** і натисніть кнопку `Відкрити`.
![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/step-6-open-sql-script-file-to-create-objects.png)

### Крок 7
Натисніть кнопку **Виконати**, щоб виконати SQL-скрипт.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/step-7-execute-the-creation-objects-script.png)

Ви повинні побачити наступний результат, який вказує на те, що запит було успішно виконано.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/step-8-result-of-creation-objects-script.png)

Якщо ви розгорнете **BikeStores > Таблиці**, ви побачите, що схеми та їхні таблиці створені, як показано нижче:

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/step-9-examine-the-tables.png)

### Крок 8
Відкрийте файл для завантаження даних у таблиці.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/step-10-open-sql-script-file-to-create-objects-Copy.png)


### Крок 9
Виберіть файл **BikeStores Sample Database – load data.sql** і натисніть кнопку Відкрити.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/step-11-open-sql-script-file-to-load-data.png)


### Крок 10
Натисніть кнопку **Виконати**, щоб завантажити дані в таблиці.

![](https://github.com/Data-Analytics-for-beginners/DataAnalyticsCourse/blob/main/IMAGES/step-13-result-of-the-data-load-script.png)


Ви повинні побачити наступне повідомлення, яке вказує на те, що всі оператори в скрипті були успішно виконані.

## Висновок

У цьому розділі лекції ви дізналися, як завантажити зразкову базу даних BikeStores у SQL Server. Ці навички дозволять вам підготувати середовище для подальшого вивчення SQL на практичних прикладах.


# 6 Налаштування Microsoft SQL Server RDS на платформі AWS



Amazon RDS (Relational Database Services) — це керований сервіс від Amazon, який дозволяє легко налаштовувати, конфігурувати та масштабувати бази даних у хмарі. Використовуючи RDS, вам не потрібно турбуватися про резервне копіювання, оновлення серверів чи додатковий дисковий простір — Amazon автоматично подбає про всі ці аспекти.

## Вхід до RDS
1. Перейдіть на aws.com/free
2. Увійдіть у свій обліковий запис AWS
3. Скористайтеся пошуком, щоб знайти RDS, або виберіть RDS з розділу нещодавно відвіданих сервісів

## Створення бази даних
1. Натисніть кнопку "Створити базу даних"
2. Виберіть стандартне створення (Standard Create), щоб скористатися безкоштовним рівнем Amazon
3. Виберіть Microsoft SQL Server як тип системи баз даних
4. Виберіть безкоштовний рівень (Free tier)
5. Вкажіть ідентифікатор бази даних (наприклад, "myrds")
6. Налаштуйте пароль адміністратора — можете обрати автоматичне генерування або створити власний
   * Цей пароль адміністратора працює як пароль SA для SQL Server
7. Натисніть "Створити базу даних"

## Налаштування публічного доступу
Щоб успішно підключитися до бази даних, необхідно дозволити публічний доступ до бази даних RDS:

1. Натисніть на ідентифікатор вашої бази даних
2. Виберіть "Змінити" (Modify)
3. Прокрутіть вниз до розділу "Підключення" (Connectivity)
4. Увімкніть опцію "Загальнодоступний доступ" (Public access)
5. Натисніть "Продовжити" (Continue)
6. Застосуйте зміни негайно (Apply immediately)

## Налаштування групи безпеки
Для безпечного підключення до вашої бази даних важливо налаштувати групу безпеки:

1. Створіть нову групу безпеки:
   * Назвіть її, наприклад, "ms-sql-sg"
   * Додайте відповідний опис
   
2. Налаштуйте правила вхідного трафіку:
   * Натисніть "Редагувати вхідні правила"
   * Додайте правило для MSSQL (порт 1433)
   * Вкажіть IP-адресу вашого комп'ютера або дозволених пристроїв
   * Збережіть правила з відповідною назвою (наприклад, "mylaptop")

3. Призначте групу безпеки вашій базі даних:
   * Перейдіть до налаштувань бази даних
   * Виберіть вашу групу безпеки в розділі підключення

## Підключення до бази даних через Management Studio
Після налаштування бази даних можна підключитися до неї через SQL Server Management Studio:

1. Знайдіть і скопіюйте кінцеву точку (endpoint) вашої бази даних в консолі RDS
2. Відкрийте SQL Server Management Studio
3. Налаштуйте підключення:
   * У поле імені сервера вставте кінцеву точку
   * У розділі автентифікації виберіть "Автентифікація SQL Server"
   * Введіть ім'я користувача (за замовчуванням "admin")
   * Введіть ваш пароль
4. Натисніть "Підключитися"

## Перевірка підключення
Щоб переконатися, що все налаштовано правильно:

1. Розгорніть розділ "Бази даних" у Management Studio
2. Спробуйте створити нову базу даних (правий клік на папці "Бази даних" → "Нова база даних")
3. Створіть тестову таблицю або запит для підтвердження роботи системи

## Додаткові рекомендації
- Для продуктивного середовища рекомендується використовувати VPC та приватні підмережі
- Налаштуйте резервне копіювання для захисту ваших даних
- Регулярно перевіряйте та оновлюйте налаштування безпеки
- Використовуйте моніторинг продуктивності для оптимізації роботи бази даних






























Посиланнння:
1) AWS RDS For SQL Server | Amazon | SQL For Developers, https://www.youtube.com/watch?v=GDPenK6EJco
2) How To Create a RDS SQL Server | AWS RDS Tutorial, https://www.youtube.com/watch?v=Vk61PZqe5lM
3) Connect Microsoft SQL database to AWS RDS | AWS Tutorial for beginners 2022, https://www.youtube.com/watch?v=Qt43du1WwmI
4) S3CloudHub, https://www.youtube.com/@S3CloudHub


