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

## Exercise 7

## Exercise 8

## Exercise 9

## Exercise 10
