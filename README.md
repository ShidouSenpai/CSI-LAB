# CSI-LAB
To insert the provided data into the defined tables, please use the following SQL commands:
sql
Copy code
-- Insert data into Product table
INSERT INTO Product (ProductID, ProductName, Price, Description) 
VALUES (1, 'iPhone 13 Pro', 999, 'The latest iPhone with advanced camera system'), 
       (2, 'Samsung Galaxy S21', 799, 'Powerful Android smartphone with high-quality display'), 
       (3, 'Google Pixel 6', 699, 'Smartphone with cutting-edge AI features and camera technology');
-- Insert data into Order table
INSERT INTO OrderTable (OrderID, OrderDate, CustomerID) 
VALUES (1, '2022-01-01', 1),
       (2, '2022-02-14', 2),
       (3, '2022-03-05', 3);
-- Insert data into OrderItem table
INSERT INTO OrderItem (OrderID, ProductID, Quantity) 
VALUES (1, 1, 2), 
       (1, 2, 1), 
       (2, 2, 3), 
       (2, 3, 2), 
       (3, 1, 1), 
       (3, 3, 1);
To query all the order information with the specified fields, please use the following SQL command:
vbnet
Copy code
SELECT OrderTable.OrderID, Product.ProductName, OrderItem.Quantity
FROM OrderTable
JOIN OrderItem ON OrderTable.OrderID = OrderItem.OrderID
JOIN Product ON OrderItem.ProductID = Product.ProductID;
This command will retrieve the OrderID, ProductName, and Quantity for all orders in the system.
