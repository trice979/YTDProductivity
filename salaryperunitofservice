select CostCenter, PPEnding, SUM(Salaries) OVER(PARTITION BY CostCenter ORDER BY PPEnding) / SUM(CurrentUOS) OVER(PARTITION BY CostCenter ORDER BY PPEnding) AS [Salary per Unit of Service]
from ProductivityBWTable
where CostCenter in (3001001037821 , 3001001031420)
and DataSet = 'actual2022'
order by CostCenter, PPEnding
