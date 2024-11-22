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
