# 1. Task 1
## 01. Database tools
```cmd
- MySql download install
- xampp downloaqd install
- datagrip (paid)
- pycharm (paid)
- Pycharm Enterprice - paid version inside available pycharm
- mysql code extention
- dbeaver ()
- mysql work bench (free)
- dbForge Studio for MySQL (crack)
- Oracle SQL Developer (free)
```
---
-- Create your first database
```sql
CREATE DATABASE class_001;
USE class_001;
<!-- Create table  -->
CREATE TABLE products (
    `id` INT AUTO_INCREMENT PRIMARY KEY,
    `name` VARCHAR(100),
    `email` VARCHAR(150),
    `password` VARCHAR(255),
    `created_at` TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```
---

-- How to comments in sql
```sql
-- mysql comment
```
-- Variable in mysql
<!-- User Define variable -->
SET @num1 = 10;
SET @num2 = 20;
SET @num3 = 50;

-- Maht in mysql
<!-- Arithmatic operation  -->
SELECT @num1 + @num2 + @num3 AS total_sum;
SELECT @num1 * @num2 * @num3 AS total_multiply;
SELECT @num3 / @num1 AS division_result;
SELECT @num3 -@num2 - @num1 AS subtraction_result;
SELECT @num3 % @num2 AS modulus_result;

<!-- SQL bitwise operations -->
SELECT @num3 & @num2 AS bitwise_and;
SELECT @num3 | @num2 AS bitwise_or;
SELECT @num3 ^ @num2 AS bitwise_xor;
SELECT ~@num2 AS bitwise_not;
SELECT @num3 << 2 AS left_shift;
SELECT @num3 >> 2 AS right_shift;
---

## 2 Built-in SQL String Functions (All in One Page)

```sql
-- 1. CHAR_LENGTH() / LENGTH()
SELECT CHAR_LENGTH('Hello, SQL!') AS char_length;
SELECT LENGTH('Hello, SQL!') AS length;

-- 2. LOWER()
SELECT LOWER('HELLO, SQL!') AS lower_case;

-- 3. UPPER()
SELECT UPPER('hello, sql!') AS upper_case;

-- 4. SUBSTRING() / SUBSTR()
SELECT SUBSTRING('Hello, SQL!', 1, 5) AS substring_result;

-- 5. TRIM()
SELECT TRIM('   SQL Tutorial   ') AS trimmed_string;

-- 6. LTRIM()
SELECT LTRIM('   SQL Tutorial') AS left_trimmed;

-- 7. RTRIM()
SELECT RTRIM('SQL Tutorial   ') AS right_trimmed;

-- 8. REPLACE()
SELECT REPLACE('Hello, World!', 'World', 'SQL') AS replaced_string;

-- 9. CONCAT()
SELECT CONCAT('Hello', ', ', 'SQL!') AS concatenated_string;

-- 10. CONCAT_WS()
SELECT CONCAT_WS('-', '2024', '10', '07') AS concatenated_with_separator;

-- 11. LEFT()
SELECT LEFT('SQL Tutorial', 3) AS left_part;

-- 12. RIGHT()
SELECT RIGHT('SQL Tutorial', 4) AS right_part;

-- 13. POSITION() / LOCATE()
SELECT POSITION('SQL' IN 'Learn SQL with tutorials') AS position_result;

-- 14. INSTR()
SELECT INSTR('Learn SQL with tutorials', 'SQL') AS instr_result;

-- 15. REVERSE()
SELECT REVERSE('SQL') AS reversed_string;

-- 16. FORMAT()
SELECT FORMAT(1234567.89, 2) AS formatted_number;

-- 17. LPAD()
SELECT LPAD('123', 5, '0') AS left_padded;

-- 18. ASCII()
SELECT ASCII('A') AS ascii_value;

-- 19. CHAR()
SELECT CHAR(65) AS character_value;
```
---

## 03. SQL Built-in Date & Time Functions Examples
```sql
-- 1. NOW() → Returns the current date and time
SELECT NOW() AS CurrentDateTime;

-- 2. CURDATE() → Returns the current date
SELECT CURDATE() AS CurrentDate;

-- 3. CURTIME() → Returns the current time
SELECT CURTIME() AS CurrentTime;

-- 4. DATE() → Extracts the date part from datetime
SELECT DATE('2024-10-03 14:30:10') AS ExtractedDate;

-- 5. TIME() → Extracts the time part from datetime
SELECT TIME('2024-10-03 14:30:10') AS ExtractedTime;

-- 6. YEAR() → Returns the year from a date
SELECT YEAR('2024-10-03') AS YearValue;

-- 7. MONTH() → Returns the month from a date
SELECT MONTH('2024-10-03') AS MonthValue;

-- 8. DAY() / DAYOFMONTH() → Returns day of month
SELECT DAY('2024-10-03') AS DayValue;
SELECT DAYOFMONTH('2024-10-03') AS DayOfMonth;

-- 9. HOUR() → Returns hour
SELECT HOUR('2024-10-03 14:30:10') AS HourValue;

-- 10. MINUTE() → Returns minute
SELECT MINUTE('2024-10-03 14:30:10') AS MinuteValue;

-- 11. SECOND() → Returns second
SELECT SECOND('2024-10-03 14:30:10') AS SecondValue;

-- 12. DATEDIFF() → Difference between two dates (days)
SELECT DATEDIFF('2024-12-25', '2024-10-03') AS DaysDifference;

-- 13. DATE_ADD() → Add interval to date
SELECT DATE_ADD('2024-10-03', INTERVAL 10 DAY) AS DatePlusTenDays;

-- 14. DATE_SUB() → Subtract interval from date
SELECT DATE_SUB('2024-10-03', INTERVAL 10 DAY) AS DateMinusTenDays;

-- 15. LAST_DAY() → Last day of month
SELECT LAST_DAY('2024-10-03') AS LastDayOfMonth;

-- 16. DAYNAME() → Weekday name
SELECT DAYNAME('2024-10-03') AS DayName;

-- 17. DAYOFWEEK() → Day index (1=Sunday, 7=Saturday)
SELECT DAYOFWEEK('2024-10-03') AS DayOfWeekIndex;

-- 18. WEEK() → Week number
SELECT WEEK('2024-10-03') AS WeekNumber;

-- 19. STR_TO_DATE() → Convert string to date
SELECT STR_TO_DATE('03-10-2024', '%d-%m-%Y') AS ConvertedDate;

-- 20. DATE_FORMAT() → Format date
SELECT DATE_FORMAT('2024-10-03 14:30:10', '%Y-%m-%d %H:%i:%s') AS FormattedDate;

-- 21. TIMESTAMPDIFF() → Difference with interval
SELECT TIMESTAMPDIFF(YEAR, '2000-01-01', '2024-10-03') AS YearDifference;

-- 22. UNIX_TIMESTAMP() → Convert to Unix timestamp
SELECT UNIX_TIMESTAMP('2024-10-03 14:30:10') AS UnixTime;

-- 23. FROM_UNIXTIME() → Convert Unix timestamp to datetime
SELECT FROM_UNIXTIME(1733217010) AS DateTimeValue;

-- 24. MAKEDATE() → Create date from year and day number
SELECT MAKEDATE(2024, 276) AS DateFromYearAndDay;

-- 25. ADDTIME() → Add time to datetime
SELECT ADDTIME('2024-10-03 10:00:00', '02:30:00') AS NewDateTime;
```
---

## 04. SQL Aggregate Functions Examples
```sql
-- COUNT() → Returns the number of rows
SELECT COUNT(*) AS TotalEmployees
FROM employee;

-- SUM() → Returns the total sum of a numeric column
SELECT SUM(salary) AS TotalSalary
FROM employee;

-- AVG() → Returns the average value
SELECT AVG(salary) AS AverageSalary
FROM employee;

-- MIN() → Returns the minimum value
SELECT MIN(salary) AS MinimumSalary
FROM employee;

-- MAX() → Returns the maximum value
SELECT MAX(salary) AS MaximumSalary
FROM employee;

-- GROUP_CONCAT() → Concatenates values from multiple rows (MySQL)
SELECT GROUP_CONCAT(name) AS EmployeeNames
FROM employee
WHERE city = 'New York';

-- Using Aggregate Functions with GROUP BY
-- Average salary by city
SELECT city, AVG(salary) AS AvgSalary
FROM employee
GROUP BY city;

-- Using HAVING with Aggregation
-- Cities where total salary is greater than 200000
SELECT city, SUM(salary) AS TotalSalary
FROM employee
GROUP BY city
HAVING SUM(salary) > 200000;
```
---

## 05. SQL Conversion Functions Examples

```sql
-- 1. CAST() → Converts a value to a specified data type
SELECT CAST('123' AS SIGNED) AS StringToInteger;
SELECT CAST(123.456 AS CHAR) AS NumberToString;
SELECT CAST('2024-01-01' AS DATE) AS StringToDate;


-- 2. CONVERT() → Similar to CAST(), also supports character set conversion

-- Convert between data types
SELECT CONVERT('123', SIGNED) AS StringToInteger;
SELECT CONVERT(123.45, CHAR) AS NumberToString;

-- Convert between character sets
SELECT CONVERT('Hello' USING utf8) AS Utf8String;


-- 3. BINARY → Converts value to binary string

SELECT BINARY 'Hello' AS BinaryString;


-- 4. FORMAT() → Formats number with decimal places and commas

SELECT FORMAT(123456.789, 2) AS FormattedNumber;


-- 5. CAST as JSON → Convert string to JSON (MySQL)

SELECT CAST('[1, 2, 3]' AS JSON) AS JsonArray;


-- 6. CONV() → Convert number from one base to another

SELECT CONV('1010', 2, 10) AS BinaryToDecimal;
SELECT CONV('A', 16, 10) AS HexToDecimal;


-- 7. TO_BASE64() and FROM_BASE64() → Encode and decode Base64

SELECT TO_BASE64('Hello World') AS EncodedBase64;
SELECT FROM_BASE64('SGVsbG8gV29ybGQ=') AS DecodedBase64;


-- 8. HEX() and UNHEX() → Convert to hexadecimal and back

SELECT HEX('Hello') AS HexValue;
SELECT UNHEX('48656C6C6F') AS OriginalString;


-- 9. DATE_FORMAT() → Format date

SELECT DATE_FORMAT(NOW(), '%Y-%m-%d') AS FormattedDate;


-- 10. TIME_TO_SEC() and SEC_TO_TIME() → Convert time and seconds

SELECT TIME_TO_SEC('02:30:00') AS TimeInSeconds;
SELECT SEC_TO_TIME(9000) AS SecondsToTime;
```
---

## 06 SQL Logical Functions Examples
```sql
-- 1. IF() → Returns value based on condition (MySQL)

SELECT IF(salary > 50000, 'High Salary', 'Low Salary') AS salary_level
FROM employee;


-- 2. IFNULL() → Returns alternative value if NULL

SELECT IFNULL(bonus, 0) AS bonus_amount
FROM employee;


-- 3. NULLIF() → Returns NULL if two expressions are equal

SELECT NULLIF(salary, 50000) AS result
FROM employee;


-- 4. CASE → Complex conditional logic (Standard SQL)

SELECT name,
CASE
    WHEN salary > 90000 THEN 'High'
    WHEN salary BETWEEN 60000 AND 90000 THEN 'Medium'
    ELSE 'Low'
END AS salary_level
FROM employee;


-- 5. COALESCE() → Returns first non-NULL value

SELECT COALESCE(bonus, allowance, 0) AS compensation
FROM employee;


-- 6. AND → Both conditions must be TRUE

SELECT *
FROM employee
WHERE salary > 60000 AND city = 'New York';


-- 7. OR → At least one condition must be TRUE

SELECT *
FROM employee
WHERE salary > 60000 OR city = 'New York';


-- 8. NOT → Negates a condition

SELECT *
FROM employee
WHERE NOT city = 'New York';


-- 9. XOR → Only one condition TRUE (MySQL)

SELECT *
FROM employee
WHERE salary > 60000 XOR city = 'New York';


-- 10. ISNULL() → Checks if value is NULL (MySQL)

SELECT *
FROM employee
WHERE ISNULL(bonus);
```
## 07. SQL JSON Functions Examples

```sql
-- 1. JSON_OBJECT() → Creates JSON object from key-value pairs
SELECT JSON_OBJECT('name', 'John', 'age', 30, 'city', 'New York') AS json_data;


-- 2. JSON_ARRAY() → Creates JSON array
SELECT JSON_ARRAY('Apple', 'Banana', 'Cherry') AS fruits;


-- 3. JSON_VALUE() → Extracts a scalar value from JSON
SELECT JSON_VALUE('{"name": "John", "age": 30}', '$.name') AS name;


-- 4. JSON_EXTRACT() → Extracts data using JSON path
SELECT JSON_EXTRACT('{"name": "John", "age": 30}', '$.age') AS age;


-- 5. JSON_SET() → Inserts or updates value
SELECT JSON_SET('{"name": "John", "age": 30}', '$.age', 31) AS updated_data;


-- 6. JSON_INSERT() → Inserts value only if key does not exist
SELECT JSON_INSERT('{"name": "John"}', '$.age', 30) AS json_data;


-- 7. JSON_REPLACE() → Replaces existing value only
SELECT JSON_REPLACE('{"name": "John", "age": 30}', '$.age', 31) AS replaced_data;


-- 8. JSON_REMOVE() → Removes key from JSON
SELECT JSON_REMOVE('{"name": "John", "age": 30}', '$.age') AS result;


-- 9. JSON_MERGE() → Merges multiple JSON documents
SELECT JSON_MERGE('{"name": "John"}', '{"age": 30}') AS merged_json;


-- 10. JSON_CONTAINS() → Checks if JSON contains value
SELECT JSON_CONTAINS('{"name": "John", "age": 30}', '{"age": 30}') AS contains_check;


-- 11. JSON_KEYS() → Returns keys of JSON object
SELECT JSON_KEYS('{"name": "John", "age": 30}') AS keys;


-- 12. JSON_LENGTH() → Number of elements or keys
SELECT JSON_LENGTH('{"name": "John", "age": 30}') AS length;


-- 13. JSON_ARRAY_APPEND() → Appends value to JSON array
SELECT JSON_ARRAY_APPEND('["Apple", "Banana"]', '$', 'Cherry') AS appended_array;


-- 14. JSON_UNQUOTE() → Removes quotes from JSON string
SELECT JSON_UNQUOTE('"Hello World"') AS unquoted_data;


-- 15. JSON_PRETTY() → Formats JSON for readability
SELECT JSON_PRETTY('{"name": "John", "age": 30}') AS pretty_json;
```
---
