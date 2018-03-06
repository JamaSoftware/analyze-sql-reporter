# Notion SQL Reporter

## About
The Notion SQL Reporter is designed to help automate the process of running SQL queries. Queries to run are placed into a folder. This program then runs those queries, and creates or updates the appropriate ingredient in Notion with the result of that query.

## Query Format Notes
Query files should be structured in the following ways:
1. a unique name - this name will be used as the key to report on the ingredient with. EX "Total Users"
2. end with the appropriate extension - '.sql' for postgres and mysql queries
3. return a single value - the result should return one row with one column. EX `select * from users limit 1;` is invalid since it return one row, but `select count(*) from users;` returns one row with one column.

## Usage
`sqlnotion [-h] --dbtype {postgres,mysql} --dbname DBNAME --user USER --password PASSWORD --host HOST --port PORT --queries-folder QUERIES_FOLDER --api-token API_TOKEN`
run `sqlnotion --help` for more information on arguments

