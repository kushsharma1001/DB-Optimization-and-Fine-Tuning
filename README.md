# Indexing-in-DB (DB Optimization and Fine Tuning)
Indexing for improving the DB operations 

https://dataschool.com/sql-optimization/how-indexing-works/

Testing the indexing advantages:
Add indexes to your table.
Run the query now:
EXPLAIN ANALYZE SELECT * FROM friends WHERE name = 'Blake';

If adding an index does not decrease query time, you can simply remove it from the database.

To remove an index use the DROP INDEX command: DROP INDEX friends_name_asc;
