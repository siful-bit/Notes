## SELECT Column FROM Table

```sql
SELECT _column1_, _column2, ..._  
FROM _table_name_;
```

Here, column1, column2, ... are the field names of the table you want to select data from. If you want to select all the fields available in the table, use the following syntax:

```sql
SELECT * FROM _table_name_;
```

here `*` denotes all. It shows every field of the data-table.

---

## SELECT only available value
The `SELECT DISTINCT` statement is used to return a list of available unique value from selected field.

```sql
SELECT DISTINCT _column1_, _column2, ..._  
FROM _table_name_;
```

```sql
SELECT DISTINCT Country FROM Customers;
```

This will return a list of unique **countries** that **Customers** table has.