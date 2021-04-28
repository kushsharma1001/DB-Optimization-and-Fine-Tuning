# Indexing-in-DB (DB Optimization and Fine Tuning)

https://dataschool.com/sql-optimization/how-indexing-works/

Testing the indexing advantages:
Add indexes to your table.
Run the query now:
EXPLAIN ANALYZE SELECT * FROM friends WHERE name = 'Blake';

If adding an index does not decrease query time, you can simply remove it from the database.

### To remove an index use the DROP INDEX {IndexName} command: DROP INDEX friends_name_asc; <br/>
### To create index: create index {name of the index} on {tableName} (Column1, Column2 ...) <br/>
Note that in multi column based index, order of columns matter. Hence, always try all permutations. <br/>
Note: We can create partial indexes also on tables: Create Index {indexName} on {tableName} (column1, column2...) where {columnName} <50;

### After a certain period, always reindex your indexes: <br/>
### a) Reindex an index: reindex index {indexName <br/>
### b) Much better is to reindex entire table: reindex table {tableName} <br/>

### Add unique constraint in a column: alter table {tableName} add constraint {constraintName} unique (columnName); <br/>

### Transactional db query: <br/>
a) https://www.sqlitetutorial.net/sqlite-transaction/ <br/>
b) https://www.sqlshack.com/transactions-in-sql-server-for-beginners/ <br/>

### Vacuum Command
    We should run vacuum verbose {tableName} to clean deleted entries from the table. 
    vacuum verbose : deletes or cleans all the tables. 

 # Explain Options
  ![image](https://user-images.githubusercontent.com/22798697/116071456-8e2f1200-a6ab-11eb-8bef-1009f5495bd4.png)
