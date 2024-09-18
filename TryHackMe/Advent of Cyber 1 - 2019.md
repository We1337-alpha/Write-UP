# Day 1 Inventory Management

![[Captura desde 2024-09-11 13-05-46.png]]

**flag: `authid`**

![[Captura desde 2024-09-11 13-05-46 1.png]]

![[Captura desde 2024-09-11 13-06-27.png]]

**flag `v4er9ll1!ss`**

![[Captura desde 2024-09-11 13-07-38.png]]

![[Captura desde 2024-09-11 13-07-56.png]]

after adding encoded cookie just reload the page

![[Captura desde 2024-09-11 13-08-22.png]]

**flag: `firewall`**
# Day 2 Arctic Forum

```bash
dirsearch -u http://0.0.0.0:0000/
```

![[Captura desde 2024-09-11 19-52-43.png]]

![[Captura desde 2024-09-11 19-54-01.png]]

**flag: `/sysadmin`**

![[Captura desde 2024-09-11 19-54-42.png]]

Search this term in google

```
Admin portal created by arctic digital design - check out our github repo
```

![[Captura desde 2024-09-11 19-56-35.png]]

![[Captura desde 2024-09-11 19-56-59.png]]

**flag: `defaultpass`**

Login with admin credentials

![[Captura desde 2024-09-11 19-58-12.png]]

**flag: `Eggnog`**
# Day 3 Evil Elf

![[Captura desde 2024-09-11 20-07-18.png]]

**flag: `63.32.89.195`**

![[Captura desde 2024-09-11 20-08-55.png]]

**flag: `ps4`**

![[Captura desde 2024-09-11 20-09-45.png]]

save this hash to file with name `hash`

```bash
$6$3GvJsNPG$ZrSFprHS13divBhlaKg1rYrYLJ7m1xsYRKxlLh0A1sUc/6SUd7UvekBOtSnSyBwk3vCDqBhrgxQpkdsNN6aYP1
```

```bash
hashcat -m 1800 hash /usr/share/wordlists/rockyou.txt --force
```

![[Captura desde 2024-09-11 20-22-23.png]]

**flag `rainbow`**
# Day 4 Training

```bash
ssh mcsysadmin@0.0.0.0 -p 22
```

Username: `mcsysadmin`
Password: `bestelf1234`

![[Captura desde 2024-09-11 21-45-53.png]]

**flag: `8`**

![[Captura desde 2024-09-11 21-47-30.png]]

**flag `recipes`**

![[Captura desde 2024-09-11 21-49-14.png]]

**flag: `file6`**

![[Captura desde 2024-09-11 21-51-18.png]]

**flag: `10.0.0.05`**

![[Captura desde 2024-09-11 21-52-31.png]]

with `root` 3 users

**flag: `3`**

![[Captura desde 2024-09-11 21-53-39.png]]

**flag: `fa67ee594358d83becdd2cb6c466b25320fd2835`**

![[Captura desde 2024-09-11 22-01-35.png]]

**flag: `$6$jbosYsU/$qOYToX/hnKGjT0EscuUIiIqF8GHgokHdy/Rg/DaB.RgkrbeBXPdzpHdMLI6cQJLdFlS4gkBMzilDBYcQvu2ro/`**
# Day 5 Ho-Ho-Hosint

![[Captura desde 2024-09-11 22-59-21.png]]

![[Captura desde 2024-09-11 23-01-06.png]]

![[Captura desde 2024-09-11 23-01-58.png]]

**flag: `December 29, 1900`**

![[Captura desde 2024-09-11 23-01-58 1.png]]

**flag: `Santa's Helper`**

![[Captura desde 2024-09-11 23-04-06.png]]

**flag: `iPhone X`**

![[Captura desde 2024-09-11 23-15-49.png]]

![[Captura desde 2024-09-11 23-16-47.png]]

![[Captura desde 2024-09-11 23-17-34.png]]

![[Captura desde 2024-09-11 23-18-52.png]]

OCTOBER 23, 2019, website show us five years of celebration 2019 - 5 = 2014

**flag: `23/10/2014`**

![[Captura desde 2024-09-11 23-21-43.png]]

reverse image search

![[Captura desde 2024-09-11 23-22-24.png]]

**flag: `ada lovelace`**

# Day 6 Data Elf-iltration

![[Captura desde 2024-09-12 18-50-45.png]]

![[Captura desde 2024-09-12 18-47-50.png]]

![[Captura desde 2024-09-12 18-48-37.png]]

**flag: `Candy Cane Serial Number 8491`**

File -> Export Objects -> HTTP choose object and save it in file

![[Captura desde 2024-09-12 18-53-11.png]]

```bash
fcrackzip -b --method 2 -D -p /usr/share/wordlists/rockyou.txt -v christmaslists.zip
```

![[Captura desde 2024-09-12 19-00-47.png]]

Password: `december`

![[Captura desde 2024-09-12 19-04-19.png]]

![[Captura desde 2024-09-12 19-05-16.png]]

**flag: `PenTester`**

```bash
stegcracked TryHackMe.jpg /usr/share/wordlists/rockyou.txt
```

![[Captura desde 2024-09-12 19-08-54.png]]

![[Captura desde 2024-09-12 19-10-21.png]]

![[Captura desde 2024-09-12 19-10-48.png]]

**flag: `RFC527`**
# Day 7 Skilling Up

```bash
nmap -p 1-999 0.0.0.0
```

![[Captura desde 2024-09-12 18-32-02.png]]

**flag: `3`**

```bash
sudo nmap -O 0.0.0.0
```

![[Captura desde 2024-09-12 18-34-24.png]]

**flag: `Linux`**

```bash
nmap -sV 0.0.0.0
```

![[Captura desde 2024-09-12 18-40-43.png]]

**flag: `7.4`**

```bash
nmap -sV 0.0.0.0
```

![[Captura desde 2024-09-12 18-40-43 1.png]]

```bash
http:0.0.0.0:999/
```

![[Captura desde 2024-09-12 18-44-16.png]]

**flag: `interesting.file`**

# Day 8 SUID Shenanigans

```bash
sudo nmap -p 1-65535 -T4 -Pn 0.0.0.0
```

![[Captura desde 2024-09-13 00-48-46.png]]

**flag: `65534`**

```bash
find / -perm /4000 -type f -exec ls -l {} \; 2>/dev/null;
```

![[Captura desde 2024-09-12 21-33-14.png]]

```bash
find /home/igor -name "flag1.txt" -exec cat {} \;
```

![[Captura desde 2024-09-12 21-32-51.png]]

**flag: `THM{d3f0708bdd9accda7f937d013eaf2cd8}`**

```bash
find / -user root -perm /4000 -exec s -ldb {} \; 2>/dev/null | grep "bin"
```

![[Captura desde 2024-09-12 23-36-33.png]]

```bash
system-control
```

![[Captura desde 2024-09-12 23-35-43.png]]

**flag: `THM{8c8211826239d849fa8d6df03749c3a2}`**

# Day 9 Requests

```python
import requests

# Starting URL and base IP
ip = "http://10.10.169.100:3000"
path = "/"

# Initialize an empty string to store the flag
flag = ""

# Loop until the "value" is 'end'
while True:
    # Send a request to the current path
    response = requests.get(ip + path)

    # Get the JSON data from the response
    data = response.json()

    # Get the value and next step
    value = data['value']
    next_path = data['next']

    # Break the loop if value is 'end'
    if value == "end":
        break

    # Append the current value to the flag
    flag += value

    # Update the path for the next request
    path = f"/{next_path}"

# Print the collected flag
print(f"Flag: {flag}")
```

![[Captura desde 2024-09-13 11-51-58.png]]

**flag: `sCrIPtKiDd`**

# Day 10 Metasploit-a-ho-ho-ho




# Day 11 Elf Applications

# Day 12 Elfcryption

# Day 13 Accumulate

# Day 14 Unknown Storage

# Day 15 LFI

# Day 16 File Confusion

# Day 17 Hydra-ha-ha-haa

# Day 18 ELF JS

# Day 19 Commands

# Day 20 Cronjob Privilege Escalation

# Day 21 Reverse Elf-ineering

# Day 22 If Santa, Then Christmas

# Day 23 LapLANd (SQL Injection)

# Day 24 Elf Stalk

# Day 25 Challenge-less