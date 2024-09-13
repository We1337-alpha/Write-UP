For modern systems using **UEFI** instead of traditional BIOS, the tool **chipsec** can be utilized to analyze and modify UEFI settings, including the disabling of **Secure Boot**. This can be accomplished with the following command:

```bash
python chipsec_main.py -module exploits.secure.boot.pk
```

- https://github.com/chipsec/chipsec
- https://chipsec.github.io/index.html