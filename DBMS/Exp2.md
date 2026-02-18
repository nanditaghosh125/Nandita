# Experiment 2 – Employee Table Queries (Retrieving Data)

## Step 1: List all DISTINCT jobs in Employee
```sql
SELECT DISTINCT job
FROM employee;
```

## Step 2: List all information about employees in Department 30
```sql
SELECT * FROM employee
WHERE deptno = 30;
```

## Step 3: Find department numbers with department number greater than 20
```sql
SELECT deptno, dname
FROM department
WHERE deptno > 20;
```

## Step 4: Find all MANAGERS and CLERKS in Department 30
```sql
SELECT * FROM employee
WHERE deptno = 30
  AND job IN ('MANAGER', 'CLERK');
```

## Step 5: List Employee name, Employee number, and department of all CLERKS
```sql
SELECT ename, empno, deptno
FROM employee
WHERE job = 'CLERK';
```

## Step 6: Find all MANAGERS NOT in Department 30
```sql
SELECT * FROM employee
WHERE job = 'MANAGER'
  AND deptno <> 30;
```

## Step 7: List employees in Department 10 who are NOT managers or clerks
```sql
SELECT *
FROM employee
WHERE deptno = 10
  AND job NOT IN ('MANAGER', 'CLERK');
```

## Step 8: Find employees earning between 1200 and 1400
```sql
SELECT ename, job, sal
FROM employee
WHERE sal BETWEEN 1200 AND 1400;
```

## Step 9: List Name and Department Number of CLERKS, ANALYSTS, SALESMEN
```sql
SELECT ename, deptno
FROM employee
WHERE job IN ('CLERK', 'ANALYST', 'SALESMAN');
```

## Step 10: List Name and Department Number of employees whose names begin with M
```sql
SELECT ename, deptno
FROM employee
WHERE ename LIKE 'M%';
```