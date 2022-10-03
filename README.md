# projet1
SELECT products.productName, products.productCode, products.quantityInStock, sum(orderdetails.quantityOrdered) from products
join orderdetails on orderdetails.productCode=products.productCode
join orders on orders.orderNumber=orderdetails.orderNumber
group by products.productName
order by sum(orderdetails.quantityOrdered) desc
LIMIT 5
