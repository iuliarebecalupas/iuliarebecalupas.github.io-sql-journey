---
title: Add, Modify and Remove Data
nav_order: 8
---

# Add, Modify and Remove Data

- ### Add Data to a table with **INSERT**

``` INSERT INTO tablename (field1, field2) VALUES (value1, value2);```

If you need to add more than a field, you can do so, by separating them with a comma '**,**', as seen in the example above. 

If you need to add more than a row, you can do so, by grouping each value/ set of values into **()**


``` INSERT INTO tablename (field1, field2) VALUES (value1, value2), (value1, value2);```


- ### Modify Data in a table with **UPDATE**

``` UPDATE tablename SET field = 'updated_data' WHERE field = 'specific_data';```

*Note!* You must be careful to use ```WHERE``` condition to specify where and what you'd like to modify something in the table, otherwise the data will be changed in the entire table.
- ### Remove a row from a table with **DELETE**
``` DELETE from table WHERE id_number = 48;```


