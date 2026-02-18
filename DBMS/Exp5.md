# Experiment 5

## Step 1: Display the total number of employees working in the company
```sql
SELECT COUNT(*)
FROM employee;
```

## Step 2: Display the total salary being paid to all employees
```sql
SELECT SUM(sal) AS total_salary
FROM employee;
```

## Step 3: Display the maximum salary from employee table
```sql
SELECT MAX(sal) AS maximum_salary
FROM employee;
```

### Step 4: Display the minimum salary from employee table
```sql
SELECT MIN(sal) AS minimum_salary
FROM employee;
```

## Step 5: Display the average salary from employee table
```sql
SELECT AVG(sal) AS average_salary
FROM employee;
```

### Step 6: Display the maximum salary being paid to Clerk

```sql
SELECT MAX(sal) AS max_clerk_salary
FROM employee
WHERE job = 'CLERK';
```

## Step 7: Display the maximum salary being paid in Department 20
```sql
SELECT MAX(sal) AS max_dept_20_salary
FROM employee
WHERE deptno = 20;
```

## Step 8: Display the minimum salary paid to any Salesman
```sql
SELECT MIN(sal) AS min_salesman_salary
FROM employee
WHERE job = 'SALESMAN';
```

## Step 9: Display the average salary drawn by Managers
```sql
SELECT AVG(sal) AS avg_manager_salary
FROM employee
WHERE job = 'MANAGER';
```

## Step 10: Display the total salary drawn by Analyst working in Department 40
```sql
SELECT SUM(sal) AS total_salary_analyst
FROM employee
WHERE job = 'ANALYST'
  AND deptno = 40;
```

## Step 11: Display the names of employees in UPPERCASE
```sql
SELECT UPPER(ename)
FROM employee;
```

## Step 12: Display the names of employees in LOWERCASE
```sql
SELECT LOWER(ename)
FROM employee;
```

## Step 13: Display the names of employees in PROPER CASE
```sql
SELECT CONCAT(
UPPER(LEFT(ename, 1)),
LOWER(SUBSTR(ename, 2))
) AS name_in_proper_case
FROM employee;
```

## Step 14: Display the length of your name using appropriate function
```sql
SELECT LENGTH('Nandita');
```

## Step 15: Display the length of all employee names
```sql
SELECT ename, LENGTH(ename)
FROM employee;
```