Print all files in the current directory, one per line (not the path, just the filename) that contain the string "500".

```bash
grep -l "500" * | xargs -n 1 basename
```

![[Captura desde 2024-09-26 08-13-59.png]]