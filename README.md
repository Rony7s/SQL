# SQL
#### Query Languages: Select, Insert, Update, Create

## SQL Problem Solutions
#### This document contains solutions to selected SQL practice problems.
### No: 2602 Basic Select
### Code 
``` MySQL
    SELECT name
    FROM customers
    WHERE state = 'RS';
```

### No: 2603 Customer Address
### Code
``` MySQL
    SELECT name, street
    FROM customers
    WHERE city = 'Porto Alegre';
```

### No: 2604 Under 10 or Greater Than 100
### Code
``` MySQL
    SELECT id, name
    FROM products
    WHERE price <10 OR price >100;
```


### No: 2615 - Expanding the Business
### Code
``` MySQL
    select distinct city
    from customers;
```

### No: 2606 - Categories
### Code
``` MySQL
    select products.id, products.name
    from products
    inner join categories
    on products.id_categories = categories.id
    where categories.name like 'super%';
```

### No: 2607 - Providers' City in Alphabetical Order
### Code
``` MySQL
    select Distinct city
    from providers
    order by city ASC;
```

### No: 2608 - Higher and Lower Price
### Code
``` MySQL
    select max(price), min(price)
    from products;
```

### No: 2609 - Products by Categories
### Code
``` MySQL
    select categories.name, sum(products.amount) as sum
    from products
    inner join categories
    on products.id_categories = categories.id
    group by categories.name;
```

### No: 2610 - Average Value of Products
### Code
``` MySQL
    select round(avg(price),2) as price
    from products;
```

### No: 2611 - Action Movies
### Code
``` MySQL
    select movies.id, movies.name
    from movies
    inner join genres
    on movies.id_genres = genres.id
    where genres.description = 'Action';
```

### No: 2613 - Cheap Movies
### Code
``` MySQL
    select movies.id, movies.name
    from movies
    inner join prices
    on movies.id_prices = prices.id
    where prices.value < 2.00;
```

### No: 2614 - September Rentals
### Code
``` MySQL
    select customers.name, rentals.rentals_date
    from customers
    inner join rentals
    on customers.id = rentals.id_customers
    where rentals.rentals_date between '2016-09-01' and '2016-09-30';
```

### No: 2615 - Expanding the Business
### Code
``` MySQL
    select distinct city
    from customers;
```


### Loading ....

<!-- ### No: 
### Code
``` MySQL
   
``` -->

<a href='https://judge.beecrowd.com/en/problems/index/9'>All Problems here</a>
