```bash
nmap -p 1-1000 0.0.0.0
```

![[Captura desde 2024-09-21 23-06-56.png]]

How many services are running under port 1000?

**flag: `2`**

![[Captura desde 2024-09-22 00-41-18.png]]

What is running on the higher port?

**flag: `ssh`**

![[Captura desde 2024-09-21 23-29-21.png]]

```bash
dirsearch -w /usr/share/wordlists/directory-list-2.3-medium.txt -u http://0.0.0.0/
```

![[Captura desde 2024-09-22 00-37-58.png]]

![[Captura desde 2024-09-21 23-33-18.png]]

![[Captura desde 2024-09-21 23-37-53.png]]

![[Captura desde 2024-09-21 23-41-14.png]]

What's the CVE you're using against the application?

**flag: `CVE-2019-9053`**

To what kind of vulnerability is the application vulnerable?

**flag: `sqli`**

Username for ftp by default: `anonymous` 

![[Captura desde 2024-09-22 00-06-06.png]]

![[Captura desde 2024-09-22 00-07-38.png]]

Username: `mitch`

```bash
hydra -l mitch -P Descargas/SecLists-master/rockyou.txt -V -t 4 0.0.0.0 ssh -s 2222 -f
```

![[Captura desde 2024-09-22 00-56-00.png]]

What's the password?

**flag: `secret`**

Where can you login with the details obtained?

**flag: `ssh`**

![[Captura desde 2024-09-22 00-58-26.png]]

What's the user flag?

**flag: `G00d j0b, keep up!`**

![[Captura desde 2024-09-22 00-59-46.png]]

Is there any other user in the home directory? What's its name?

**flag: `sunbath`**

![[Captura desde 2024-09-22 01-05-18.png]]

What can you leverage to spawn a privileged shell?

**flag: `vim`**

![[Captura desde 2024-09-22 01-02-43.png]]

What's the root flag?

**flag: `W3ll d0n3. You made it!`**