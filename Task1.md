SELECT CustomerName FROM Customers WHERE Country = 'UK';

SELECT productName, Unit, Price
FROM Products
WHERE Price >= 55;

SELECT ProductName, Price, CategoryName FROM Products INNER JOIN Categories ON Products.CategoryID = Categories.CategoryID WHERE Categories.CategoryID = 1 ORDER BY Price ASC;

SELECT FirstName, LastName, Orders.OrderID FROM Employees INNER JOIN Orders ON Employees.EmployeeID = Orders.EmployeeID WHERE Employees.EmployeeID Between 1 AND 5 ORDER BY LastName ASC;

SELECT CustomerName, Orders.OrderID, ProductName, Quantity FROM ((Customers INNER JOIN Orders ON Customers.CustomerID = Orders.CustomerID) INNER JOIN OrderDetails ON OrderDetails.OrderID=Orders.OrderID) INNER JOIN Products ON Products.ProductID=OrderDetails.ProductID ORDER BY CustomerName ASC;
