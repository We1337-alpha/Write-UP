```bash
sudo nmap -F -sSV -O 0.0.0.0
```

![[Captura desde 2024-09-14 22-00-01.png]]

visiting site there few credentails

```text
Sr. System Admin: Adam Adams - adamsa@herot.net  
System Admin (Intern): Bob Banter - banterb@herot.net  
System Admin: Chad Coffee - coffeec@herot.net
```

```bash
nmap -p 1-65535 -T4 -A 0.0.0.0
```

![[Captura desde 2024-09-25 23-58-27.png]]

```bash
ftp ftp://anonymous:anonymous@0.0.0.0
```

