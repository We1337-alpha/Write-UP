There are files in this challenge with different file extensions. Remove all files with the .doc extension recursively in the current working directory.

```bash
find . -type f -name "*.doc" -exec rm -f {} \;
```

![[Captura desde 2024-09-26 07-56-55.png]]