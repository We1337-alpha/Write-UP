```bash
sudo nmap 0.0.0.0 -F
sudo nmap 0.0.0.0 -F -sV
```

![[Captura desde 2024-09-09 15-37-21.png]]

```bash
dirb http://0.0.0.0 > output.txt
```


![[Captura desde 2024-09-22 02-44-16.png]]

Exploit: [https://github.com/AssassinUKG/fuleCMS](https://github.com/AssassinUKG/fuleCMS)

```bash
python exploit.py 0.0.0.0:00
```

![[Captura desde 2024-08-30 14-45-30.png]]

Privilgage escaltion