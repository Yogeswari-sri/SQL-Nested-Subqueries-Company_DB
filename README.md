# SQL-Nested-Subqueries-Company_DB

Nested subqueries are queries placed inside another query, often in the WHERE, FROM, or SELECT clause, to perform complex filtering or calculations. They allow breaking down problems into smaller steps and combining results for advanced data analysis.

📘 Key Highlights
Definition: A subquery inside another subquery or main query.

Usage: Helps in filtering, aggregation, and comparisons when direct joins or simple queries aren’t sufficient.

Types:

Scalar Subquery – returns a single value.

Row Subquery – returns a single row with multiple columns.

Table Subquery – returns multiple rows and columns.

🛠 Example

-- Find employees earning more than the average salary in their department
SELECT emp_name, salary, dept_id
FROM employees e
WHERE salary > (
    SELECT AVG(salary)
    FROM employees
    WHERE dept_id = e.dept_id
);
OUTPUT
<img width="1598" height="719" alt="image" src="https://github.com/user-attachments/assets/13ff6c44-a5f7-4082-8e13-96fe60658e6c" />

🚀 Why It Matters
Enables multi-level filtering without complex joins.

Improves query modularity by breaking logic into smaller parts.

Essential for data analysts to handle hierarchical queries and advanced reporting.
