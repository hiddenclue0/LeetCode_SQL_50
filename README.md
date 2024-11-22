https://leetcode.com/problems/recyclable-and-low-fat-products/
-- 1757. Recyclable and Low Fat Products

	select product_id
	from Products
	where low_fats = 'Y' and recyclable = 'Y'


https://leetcode.com/problems/find-customer-referee/
-- 584. Find Customer Referee

	select name 
	from Customer
	where referee_id != 2 or referee_id is null


https://leetcode.com/problems/big-countries/
-- 595. Big Countries
	
	select name, population, area 
	from World
	where area >= 3000000 or population >=25000000


https://leetcode.com/problems/article-views-i/
-- 1148. Article Views I

	select DISTINCT author_id as id 
	from Views 
	where (author_id = viewer_id) 
	order by author_id asc


https://leetcode.com/problems/invalid-tweets/
-- 1683. Invalid Tweets

	select tweet_id 
	from Tweets 
	where length(content)>15
