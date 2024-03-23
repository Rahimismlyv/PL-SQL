create table emp_copy as select * from hr.employees;
/
create table salary_change_history (employee_id number, change_date date , salary number)    
/
create or replace trigger trg_sal_change
before update of salary on emp_copy
for each row
begin
	insert into salary_change_history values (:old.employee_id,sysdate,:old.salary);
end;
