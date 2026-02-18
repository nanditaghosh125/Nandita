# Experiment 4

## Step 1: Display the list of employees who have joined the company before 30th June 1980 or after 31st December 1981
```sql
SELECT * FROM employee
WHERE hiredate < '1980-06-30'
   OR hiredate > '1981-12-31';
```

## Step 2: Display the names of employees whose names have second alphabet 'A'
```sql
SELECT ename
FROM employee
WHERE ename LIKE '_A%';
```

## Step 3: Display the names of employees whose name is exactly five characters in length
```sql
SELECT ename
FROM employee
WHERE ename LIKE '_____';
```

## Step 4: Display the names of employees whose names have second last alphabet E
```sql
SELECT ename
FROM employee
WHERE ename LIKE '%E_';
```

## Step 5: Display the names of employees who are not working as Salesman or Clerk or Analyst
```sql
SELECT ename
FROM employee
WHERE job NOT IN ('SALESMAN', 'CLERK', 'ANALYST');
```

## Step 6: Display the name of the employee along with their annual salary (SAL * 12). The name of the employee earning highest salary should appear first
```sql
SELECT ename, (sal * 12) AS annual_salary
FROM employee
ORDER BY annual_salary DESC;
```

## Step 7: Display name, salary, HRA, DA, PF, and total salary for each employee
```sql
SELECT 
    ename, sal,
    (sal + sal*0.15 + sal*0.10 - sal*0.05) AS total_salary
    (sal * 0.15) AS hra,
    (sal * 0.10) AS da,
    (sal * 0.05) AS pf,
FROM employee;
```

## Step 8: Update the salary of each employee by 10% increment who are not eligible for commission
```sql
UPDATE employee
SET sal = sal + (0.10 * sal)
WHERE comm IS NULL
   OR comm = 0;
```

## Step 9: Display those employees whose salary is more than 3000 after giving 20% increment
```sql
SELECT * FROM employee
WHERE sal * 1.20 > 3000;
```

## Step 10: Display those employees whose salary contains at least 3 digits
```sql
SELECT * FROM employee
WHERE sal > 99;
```

