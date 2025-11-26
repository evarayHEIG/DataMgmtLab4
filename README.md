# DataMgmtLab4

## Exercise 1

## Exercise 2

```sql
SELECT dg.EnglishCountryRegionName
FROM dimcustomer dc 
JOIN dimgeography dg 
ON dc.GeographyKey = dg.GeographyKey
```

![alt text](images/ex2.png)

## Exercise 3

## Exercise 4

```sql
SELECT ds.ResellerName, SUM(frs.TotalProductCost) as Profit
FROM dimreseller ds 
JOIN factresellersales frs 
ON ds.ResellerKey = frs.ResellerKey
GROUP BY ds.ResellerName
ORDER BY Profit DESC 
```

![](images/ex4.png)

## Exercise 5

## Exercise 6

```sql
SELECT frs.OrderQuantity, d.FullDateAlternateKey AS SaleDate, pc.EnglishProductCategoryName AS Category
FROM factresellersales frs
JOIN dimdate d
ON frs.DueDateKey = d.DateKey
JOIN dimproduct p
ON frs.ProductKey = p.ProductKey
JOIN dimproductsubcategory psc
ON p.ProductSubcategoryKey = psc.ProductSubcategoryKey
JOIN dimproductcategory pc
ON psc.ProductCategoryKey = pc.ProductCategoryKey
```

![](images/ex6.png)

## Exercise 7

## Exercise 8

```sql
SELECT fis.OrderQuantity AS 'Order Quantity', d.FullDateAlternateKey AS 'Delivery Date', fis.CustomerKey AS 'Customer Id'
FROM factinternetsales fis
JOIN dimdate d
ON fis.DueDateKey = d.DateKey
```

![](images/ex8.png)

And another screenshot that shows values > 7.

![](images/ex8_2.png)

## Exercise 9

## Exercise 10
