Print all matching lines (without the filename or the file path) in all files under the current directory that start with "access.log" that contain the string "500".

Note that there are no files named `access.log` in the current directory, you will need to search recursively.

```bash
grep -rh "500" **/access.log*
```

![[Captura desde 2024-09-26 08-23-49.png]]