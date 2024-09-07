```bash
nmap -A -Pn -sV 0.0.0.0
```

![[Captura desde 2024-09-07 14-15-25.png]]

```bash
sudo dirb http://0.0.0.0:00 -o output.txt
```

```bash
cat output.txt
```

```bash
http://0.0.0.0:00/robots
```

![[Captura desde 2024-09-07 16-49-12.png]]

```bash
http://0.0.0.0:00/key-1-of-3.txt
```

![[Captura desde 2024-09-07 16-52-13.png]]

```bash
wget http://0.0.0.0:00/fsocity.dic
```

