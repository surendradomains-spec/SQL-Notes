DISTINCT keyword
  ->  The DISTINCT keyword is used in SQL to remove duplicate values from the result of a SELECT query.
                (OR)
  -> DISTINCT shows only unique (non-repeated) values.

Syntax
    SELECT DISTINCT column_name
    FROM table_name;
Example with Table
Table: students
    | id | name  | city   |
    | -- | ----- | ------ |
    | 1  | Ravi  | Delhi  |
    | 2  | Anya  | Mumbai |
    | 3  | Kiran | Delhi  |
    | 4  | John  | Mumbai |

✅ Without DISTINCT
    SELECT city
    FROM students;
Output
    | city   |
    | ------ |
    | Delhi  |
    | Mumbai |
    | Delhi  |
    | Mumbai |
-> Duplicates are shown.

✅ With DISTINCT
    SELECT DISTINCT city
    FROM students;
Output
    | city   |
    | ------ |
    | Delhi  |
    | Mumbai |

->  Duplicate values are removed.

✅ DISTINCT with Multiple Columns
    SELECT DISTINCT name, city
    FROM students;
    -> Here, uniqueness is checked based on the combination of both columns.
Example Output
    | name  | city   |
    | ----- | ------ |
    | Ravi  | Delhi  |
    | Anya  | Mumbai |
    | Kiran | Delhi  |
    | John  | Mumbai |
-> Rows are considered duplicates only if both columns match.
