Find Employee who are managers as well
EmpId, EmpName, ManagerId, Salary

101, Purvi, 100, x
102, Nishant, 101, y


----


SELECT e.EmpName  
FROM Employee e
JOIN Employee m
where e.id = m.id;