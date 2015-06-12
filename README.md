1.How many users are there? SELECT count(id) FROM users; 49 users

2.What are the 5 most expensive items? SELECT * FROM items order by price desc limit 5;

3.What's the cheapest electronics item? SELECT * FROM items WHERE catagory="Electronics" order by price asc limit 1;

4.Who lives at "489 Fritsch Island"? Do they have another address? SELECT * FROM addresses WHERE street="489 Fritch Island"; SELECT * FROM users JOIN addresses ON user.id = addresses.user_id WHERE user_id = 35;

5.Correct Tevin Mitchell's New York zip code to 10108. SELECT * FROM users WHERE first_name="Tevin"; UPDATE addresses SET zip="10108" WHERE user_id=25 and state="New York";

6.How much would it cost to buy one of each piece of jewelery? "SELECT sum(price)FROM items"

7.How many total items did we sell? SELECT sum(quantity) FROM orders;

8.How much was spent on health? 
SELECT sum(items.price * orders.quantity) FROM orders JOIN items ON items.id = orders.item_id WHERE category="Health";
1796.20 was spent on Health;

9.Simulate buying an item by inserting a User for yourself and an Order for that User (do not include this in the figures above).
INSERT INTO users VALUES (null,"Patrick","Nielsen","ptnielsen55@gmail.com");" to insert myself as a user and created an order for myself for 5 Awesome Steel Computers using "INSERT INTO orders VALUES (null,51,19,5);