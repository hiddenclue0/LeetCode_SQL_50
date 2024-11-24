<h1> SQL 50 - LeetCode </h1>
<h2> Solutions for SQL 50 Study Plan on LeetCode </h2>	


https://leetcode.com/problems/recyclable-and-low-fat-products/
<br>1757. Recyclable and Low Fat Products
```sql
	select product_id
	from Products
	where low_fats = 'Y' and recyclable = 'Y'
```


https://leetcode.com/problems/find-customer-referee/
<br>584. Find Customer Referee
```sql
	select name 
	from Customer
	where referee_id != 2 or referee_id is null
```

https://leetcode.com/problems/big-countries/
<br>595. Big Countries
```sql
	select name, population, area 
	from World
	where area >= 3000000 or population >=25000000
```

https://leetcode.com/problems/article-views-i/
<br>1148. Article Views I
```sql
	select DISTINCT author_id as id 
	from Views 
	where (author_id = viewer_id) 
	order by author_id asc
```

https://leetcode.com/problems/invalid-tweets/
<br>1683. Invalid Tweets
```sql
	select tweet_id 
	from Tweets 
	where length(content)>15
```

https://leetcode.com/problems/replace-employee-id-with-the-unique-identifier/
<br>1378. Replace Employee ID With The Unique Identifier
```sql
	# Write your MySQL query statement below
	select unique_id , name from Employees E left join EmployeeUNI Eu
	on e.id = eu.id
```

https://leetcode.com/problems/product-sales-analysis-i/
<br>1068. Product Sales Analysis I
```sql
	select  product_name, year, price 
	from Sales s 
	join Product p
	on s.product_id = p.product_id 
```

https://leetcode.com/problems/customer-who-visited-but-did-not-make-any-transactions/
<br>1581. Customer Who Visited but Did Not Make Any
```sql
	select customer_id , count(customer_id ) as count_no_trans 
	from Visits v
	left join Transactions t 
	on v.visit_id = t.visit_id 
	where t.visit_id is null
	group  by customer_id
```

https://leetcode.com/problems/rising-temperature/
<br>197. Rising Temperature
```sql
	select a.id
	from Weather a
	join Weather b
	on a.recordDatedate_add(b.recordDate, interval 1 day)
	where b.temperature < a.temperature 
```

https://leetcode.com/problems/employee-bonus/
<br>577. Employee Bonus
```sql
	SELECT w1.id 
	FROM Weather w1, Weather w2
	WHERE DATEDIFF(w1.recordDate, w2.recordDate) = 1
	AND w1.temperature > w2.temperature

	-- OR
	SELECT w1.id
	FROM Weather w1, Weather w2
	WHERE w1.temperature > w2.temperature
	AND SUBDATE(w1.recordDate, 1) = w2.recordDate
```


https://leetcode.com/problems/employee-bonus/
<br>577. Employee Bonus
```sql
	SELECT machine_id, ROUND(AVG(end - start), 3) AS processing_time
	FROM 
	(SELECT machine_id, process_id, 
		MAX(CASE WHEN activity_type = 'start' THEN timestamp END) AS start,
		MAX(CASE WHEN activity_type = 'end' THEN timestamp END) AS end
	 FROM Activity 
	  GROUP BY machine_id, process_id) AS subq
	GROUP BY machine_id
```

https://leetcode.com/problems/employee-bonus/
<br>577. Employee Bonus
```sql
SELECT w1.id 
FROM Weather w1, Weather w2
WHERE DATEDIFF(w1.recordDate, w2.recordDate) = 1
AND w1.temperature > w2.temperature

-- OR
SELECT w1.id
FROM Weather w1, Weather w2
WHERE w1.temperature > w2.temperature
AND SUBDATE(w1.recordDate, 1) = w2.recordDate
```
