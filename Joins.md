___________________________________________________________________
# JOINING TABLES to find the TOP 5 CUSTOMERS of the TOP 10 CITIES
___________________________________________________________________


```
SELECT A.customer_id, B.first_name, B.last_name, E.country, D.city,
	SUM(amount) AS total_paid
FROM payment A
INNER JOIN customer B ON A.customer_id = B.customer_id
INNER JOIN address C ON B.address_id = C.address_id
INNER JOIN city D ON C.city_id = D.city_id
INNER JOIN country E ON D.country_id = E.country_id 
WHERE E.country IN ('India', 'China', 'United States', 'Japan', 'Mexico', 'Brazil', 'Russian Federation', 'Philippines', 'Turkey', 'Indonesia')
AND D.city IN ('Aurora', 'Tokat', 'Tarsus', 'Atlixco', 'Emeishan', 'Pontianak', 'Shimoga', 'Aparecida de Goinia', 'Zalantun', 'Taguig')
GROUP BY A.customer_id, B.first_name, B.last_name, E.country, D.city
ORDER BY total_paid DESC
LIMIT 5
![image](https://user-images.githubusercontent.com/104154067/164773328-90eed144-588f-4a40-92c4-6994c3d151cc.png)

```