# Blink-It-Project
Blink It Project Using Mysql...

show databases;

create database BLINKIT;

use blinkit;

use blinkit;
#1. Import Data from table Grocery Sales using the provided CSV File.
#2.Write an SQL query to show all Item_Identifier

select item_identifier from blinkit;

#3. Write an SQL query to show count of total Item_Identifier. 
select count(item_identifier) from blinkit ;

#4. Write an SQL query to show maximum Item Weight. 
select max(item_weight) from blinkit;

#5. Write an SQL query to show minimum Item Weight. 
select min(item_weight) from blinkit;

#6. Write an SQL query to show average Item_Weight. 
select ceil(avg(item_weight)) from blinkit;

#7. Write an SQL query to show count of Item_Fat_Content WHERE Item_Fat_Content is Low Fat. 
select count(item_fat_content) from blinkit where Item_Fat_Content='low fat';

#8. Write an SQL query to show count of Item_Fat_Content WHERE Item_Fat_Content is Regular. 
select count(item_fat_content) from blinkit b where Item_Fat_Content='regular';

#9. Write an SQL query to show maximum Item_MRP 
select max(item_mrp) from blinkit;

#10. Write an SQL query to show minimum Item_MRP 
select min(item_mrp) from blinkit b ;

#11. Write an SQL query to show Item_Identifier , Item_Fat_Content ,Item_Type, Item_MRP whose Item_MRP is greater than 200. 
select item_identifier,item_fat_content,item_type,item_mrp from blinkit b where item_mrp>200;

#12.Write an SQL query to show maximum Item_MRP WHERE Item_Fat_Content is Low Fat 
select *,max(item_mrp) from blinkit b where Item_Fat_Content='low fat'

#13. Write an SQL query to show minimum Item_MRP whose Item_Fat_Content is Low Fat 
select *,min(item_mrp) from blinkit b where item_fat_content='low fat';

#14. Write an SQL query to show ALL DATA WHERE item MRP is BETWEEN 50 to 100 
select * from blinkit b where item_mrp between 50 and 100;

#15. Write an SQL query to show ALL UNIQUE value of Item_Fat_Content 
select distinct(item_fat_content) from blinkit b;

#16. Write an SQL query to show ALL UNIQUE value of Item_Type 
select distinct(item_type) from blinkit b ;

#17. Write an SQL query to show ALL DATA in descending ORDER by Item MRP 
select * from blinkit b order by item_mrp desc;

#18. Write an SQL query to show ALL DATA in ascending ORDER by Item_Outlet_Sales 
select * from blinkit b order by Item_Outlet_Sales;

#19. Write an SQL query to show ALL DATA in ascending by Item_Type 
select * from blinkit b order by Item_Type ;

#20. Write an SQL query to show DATA of item_type dairy & Meat 
select * from blinkit b where Item_Type in ('dairy','meat');

#21. Write an SQL query to show ALL UNIQUE value of Outlet_Size 
select distinct(outlet_size) from blinkit b ;

#22. Write an SQL query to show ALL UNIQUE value of Outlet_Location_Type 
select distinct(outlet_location_type) from blinkit b ;

#23. Write an SQL query to show ALL UNIQUE value of Outlet_Type 
select distinct(outlet_type) from blinkit b ;

#*24. Write an SQL query to show count of number of items by Item_Type and order it in descending order 
SELECT item_type,COUNT(item_type) from blinkit b group by  item_type order by count(item_type) desc ;

#25. Write an SQL query to show count of number of items by Outlet_Size and ordered it in ascending order 
select outlet_size, count(outlet_size) from blinkit b group by outlet_size order by outlet_size;

#26. Write an SQL query to show count of number of items by Outlet_Type and ordered it in descending order. 
select count(outlet_type),outlet_type from blinkit group by outlet_type order by count(outlet_type) desc;

#27. Write an SQL query to show count of items by Outlet_Location_Type and order it indescending order 
select outlet_location_type,count(outlet_location_type) from blinkit b group by outlet_location_type order by count(outlet_location_type)desc;

#28. Write an SQL query to show maximum MRP by Item_Type 
select max(item_mrp),item_type as Maximum_MRP from blinkit b group by item_type;

#29. Write an SQL query to show minimum MRP by Item_Type 
select item_type,min(item_mrp) from blinkit b group by item_type;

#30. Write an SQL query to show minimum MRP by Outlet_Establishment_Year and order it in descending order. 
select outlet_establishment_year,min(item_mrp) from blinkit b group by Outlet_Establishment_Year order by Outlet_Establishment_Year desc;

#31. Write an SQL query to show maximum MRP by Outlet_Establishment_Year and order it in descending order. 
select outlet_establishment_year,max(item_mrp) from blinkit b group by Outlet_Establishment_Year order by Outlet_Establishment_Year desc;

#32. Write an SQL query to show average MRP by Outlet_Size and order it in descending order. 
select outlet_size,avg(item_mrp) from blinkit group by Outlet_Size order by avg(item_mrp) desc;

#33. Write an SQL query to Average MRP by Outlet_Type and ordered in ascending order. 
select outlet_type,avg(item_mrp) from blinkit b group by Outlet_Type order by avg(item_mrp);

#34. Write an SQL query to show maximum MRP by Outlet_Type 
select max(item_mrp),Outlet_Type  from blinkit b group by Outlet_Type;

#35. Write an SQL query to show maximum Item_Weight by Item_Type 
select max(item_weight),item_type from blinkit b group by item_type;

#36. Write an SQL query to show maximum Item_Weight by Outlet_Establishment_Year 
select outlet_establishment_year, max(item_weight),item_type
from blinkit b group by Outlet_Establishment_Year ;

#37. Write an SQL query to show minimum Item_Weight by Outlet_Type 
select item_type,min(item_weight) from blinkit b group by Outlet_Type ;

#38. Write an SQL query to show average Item_Weight by Outlet_Location_Type and arrange it by descending order 
select outlet_location_type,avg(item_weight) from blinkit b group by outlet_location_type order by avg(item_weight) desc;

#39. Write an SQL query to show maximum Item_Outlet_Sales by Item_Type 
select max(item_outlet_sales),item_type from blinkit b group by item_type;

#40. Write an SQL query to show minimum Item_Outlet_Sales by Item_Type 
select min(item_outlet_sales),item_type from blinkit b group by item_type;

#41. Write an SQL query to show minimum Item_Outlet_Sales by Outlet_Establishment_Year
select min(item_outlet_sales),Outlet_Establishment_Year  from blinkit b group by Outlet_Establishment_Year ;

#42. Write an SQL query to show maximum Item_Outlet_Sales by Outlet_Establishment_Year and order it by descending order 
select max(item_outlet_sales),Outlet_Establishment_Year  from blinkit b group by Outlet_Establishment_Year order by Outlet_Establishment_Year desc;

#43. Write an SQL query to show average Item_Outlet_Sales by Outlet_Size and order it it descending order 
select avg(item_outlet_sales), outlet_size from blinkit b group by Outlet_Size order by Outlet_Size desc;

#44. Write an SQL query to show average Item_Outlet_Sales by Outlet_Type 
select avg(item_outlet_sales),outlet_type from blinkit b group by Outlet_Type ;

#45. Write an SQL query to show maximum Item_Outlet_Sales by Outlet_Type 
select max(item_outlet_sales),outlet_type from blinkit b group by Outlet_Type;

#46. Write an SQL query to show total Item_Outlet_Sales by Item_Type 
select sum(item_outlet_sales),Item_Type  from blinkit b group by item_type;

#47. Write an SQL query to show total Item_Outlet_Sales by Item_Fat_Content 
select sum(item_outlet_sales),Item_Fat_Content  from blinkit b group by Item_Fat_Content;

#48. Write an SQL query to show maximum Item_Visibility by Item_Type 
select max(item_visibility), item_type from blinkit b group by Item_Type ;

#49. Write an SQL query to show Minimum Item_Visibility by Item_Type
select min(item_visibility), item_type from blinkit b group by Item_Type ;

#50. Write an SQL query to show total Item_Outlet_Sales by Item_Type but only WHERE Outlet_Location_Type is Tier 1 
select count(item_outlet_sales), item_type from blinkit b where Outlet_Location_Type='tier 1' group by Item_Type ;

#51. Write an SQL query to show total Item_Outlet_Sales by Item_Type WHERE Item_Fat_Content is ONLY Low Fat & LF 
select count(item_outlet_sales), item_type from blinkit b where Item_Fat_Content ='low fat' group by Item_Type 
