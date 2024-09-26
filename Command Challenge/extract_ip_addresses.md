Extract all IP addresses from files that start with "access.log" printing one IP address per line.

```bash
grep -h -o -E '([0-9]{1,3}\.){3}[0-9]{1,3}' **/access.log* | sort -u
```

![[Captura desde 2024-09-26 09-21-14.png]]