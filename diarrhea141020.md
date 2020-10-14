## Diary Entry | 14.10.2020

Dear Diary,

contrary to your actual purpose, I will now use you for some SQL exercises. Don't be mad, you are not a joke to me. I luv chu.


# SELECT

1.: SELECT last_name, job_id, hire_date AS start_date, employee_id
    FROM employees;

2.: SELECT DISTINCT job_id FROM employees

3.: SELECT 
    last_name, salary 
    FROM 
    employees
    WHERE
    salary > 12000

4.: SELECT 
    last_name, department_id
    FROM
    employees
    WHERE
    employee_id = 176

5.: SELECT 
    last_name, job_id, hire_date
    FROM
    employees
    ORDER BY
    hire_date ASC

6.: SELECT
    last_name, department_id
    FROM
    employees
    WHERE
    department_id = 20
    ORDER BY
    last_name ASC

7.: SELECT
    last_name, salary, comission_pct
    FROM
    employees
    WHERE
    comission_pct = 20


# Join

1.: SELECT
    SUM(salary), job_id
    FROM
    employees
    GROUP BY
    job_id
    ORDER BY
    SUM(salary) DESC

2.: SELECT
    AVG(salary)
    FROM
    employees

3.: SELECT first_name, last_name, department_name FROM employees JOIN departments ON employees.department_id = departments. department name

4.: SELECT 
    department_name, postal_code, city, state_province, street_adress
    FROM
    departments JOIN locations
    ON
    departments.location_id = locations.location_id

5.: SELECT 
    department_name, postal_code, city, state_province, street_adress, country_name
    FROM
    departments JOIN locations JOIN countries
    ON
    departments.location_id = locations.location_id, locations.counrty_id=countries.counrty_id

6.:SELECT 
    department_name, postal_code, city, state_province, street_adress, country_name, first_name, last_name
    FROM
    employees JOIN departments JOIN locations JOIN countries
    ON
    departments.location_id = locations.location_id, locations.counrty_id=countries.counrty_id, departments.manager_id = employees.manager_id



