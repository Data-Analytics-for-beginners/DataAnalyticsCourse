

# Знаходження другої найвищої зарплати

Розглянемо важливе питання для співбесід з SQL – як знайти другу найвищу зарплату в таблиці. Це завдання часто зустрічається на технічних інтерв'ю.

## Підготовка бази даних
Спочатку створимо нову базу даних для наших прикладів:

```sql
CREATE DATABASE AdvancedSQLQuestions;
USE AdvancedSQLQuestions;
```

Тепер створимо таблицю `Employees` та заповнимо її даними:

```sql
CREATE TABLE Employees (
    Id INT,
    Name VARCHAR(50),
    Salary INT
);

INSERT INTO Employees VALUES
    (1, 'Співробітник1', 80000),
    (2, 'Співробітник2', 90000),
    (3, 'Співробітник3', 85000),
    (4, 'Співробітник4', 95000),
    (5, 'Співробітник5', 70000),
    (6, 'Співробітник6', 75000),
    (7, 'Співробітник7', 60000),
    (8, 'Співробітник8', 98000),
    (9, 'Співробітник9', 65000),
    (10, 'Співробітник10', 88000);
```

## Метод 1: Використання підзапитів

Перший підхід використовує підзапити. Спочатку знайдемо максимальну зарплату:

```sql
SELECT MAX(Salary) FROM Employees;
```

Тепер модифікуємо запит, щоб знайти другу найвищу зарплату:

```sql
SELECT MAX(Salary) AS [Друга найвища зарплата]
FROM Employees
WHERE Salary < (SELECT MAX(Salary) FROM Employees);
```

Якщо потрібно знайти третю найвищу зарплату:

```sql
SELECT MAX(Salary) AS [Третя найвища зарплата]
FROM Employees
WHERE Salary < (
    SELECT MAX(Salary) 
    FROM Employees 
    WHERE Salary < (SELECT MAX(Salary) FROM Employees)
);
```

## Метод 2: Використання CTE та функції DENSE_RANK()

Другий підхід використовує загальні табличні вирази (CTE) разом із функцією DENSE_RANK():

```sql
WITH CTE AS (
    SELECT Salary, DENSE_RANK() OVER (ORDER BY Salary DESC) AS DR
    FROM Employees
)
SELECT Salary AS [Друга найвища зарплата]
FROM CTE
WHERE DR = 2;
```

Для третьої найвищої зарплати:

```sql
WITH CTE AS (
    SELECT Salary, DENSE_RANK() OVER (ORDER BY Salary DESC) AS DR
    FROM Employees
)
SELECT Salary AS [Третя найвища зарплата]
FROM CTE
WHERE DR = 3;
```

## Метод 3: Підзапити з DENSE_RANK()

Третій підхід використовує підзапити з функцією DENSE_RANK():

```sql
SELECT Salary AS [Друга найвища зарплата]
FROM (
    SELECT Salary, DENSE_RANK() OVER (ORDER BY Salary DESC) AS DR
    FROM Employees
) X
WHERE DR = 2;
```

Для третьої найвищої зарплати:

```sql
SELECT Salary AS [Третя найвища зарплата]
FROM (
    SELECT Salary, DENSE_RANK() OVER (ORDER BY Salary DESC) AS DR
    FROM Employees
) X
WHERE DR = 3;
```

## Метод 4: Підзапити з TOP

Четвертий підхід використовує підзапити з ключовим словом TOP:

```sql
SELECT TOP 1 Salary AS [Друга найвища зарплата]
FROM (
    SELECT DISTINCT TOP 2 Salary
    FROM Employees
    ORDER BY Salary DESC
) X
ORDER BY Salary ASC;
```

Для третьої найвищої зарплати:

```sql
SELECT TOP 1 Salary AS [Третя найвища зарплата]
FROM (
    SELECT DISTINCT TOP 3 Salary
    FROM Employees
    ORDER BY Salary DESC
) Y
ORDER BY Salary ASC;
```

## Висновок
Ми розглянули чотири різні підходи до знаходження n-ої найвищої зарплати в SQL:
1. Використання підзапитів
2. Використання CTE з DENSE_RANK()
3. Підзапити з DENSE_RANK()
4. Підзапити з TOP

