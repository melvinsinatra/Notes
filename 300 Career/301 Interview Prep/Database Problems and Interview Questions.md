
## N+1 Query

Performance anti-pattern where an application executes **1 query to fetch a list of records**, and then **N additional queries to fetch related data for each record**, resulting in **N+1 total queries**.
### Example
You want to fetch all users and their orders.

#### Inefficient approach (N+1 problem)
```
SELECT * FROM Users; -- 1 query
```

Then for each user:
```
SELECT * FROM Orders WHERE user_id = x;  -- N queries
```

If you have 100 users:
- 1 query for users
- 100 queries for orders  
-  **101 total queries**
#### Why This Is Bad
- Excessive **database round-trips**
- Increased **latency** due to **CPU + IO load**
- Bloating cloud **costs**
- Poor **scalability**

#### Correct Approach (Single Query Using JOIN)
```
SELECT u.*, o.*
FROM Users u
LEFT JOIN Orders o ON u.id = o.user_id;
```