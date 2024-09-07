```bash
sudo nmap -sV -Pn -F 0.0.0.0
```

![[Captura desde 2024-09-06 18-02-35.png]]

```
dirb http://0.0.0.0:0000
```

![[Captura desde 2024-09-06 18-03-51.png]]

this link will open prompt `http://0.0.0.0:0000/host-manager` but cancel it it will show page with credentials

![[Captura desde 2024-09-07 09-27-46.png]]

Username: `tomcat`
Password: `s3cret`

