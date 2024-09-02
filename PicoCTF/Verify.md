# Verify

link [https://play.picoctf.org/practice/challenge/450?page=1](https://play.picoctf.org/practice/challenge/450?page=1)

```bash
find files/ -type f -exec sh -c 'echo "==> {} <=="; cat "{}"' \;
```

![[Captura desde 2024-08-31 18-52-40.png]]

```bash
openssl enc -d -aes-256-cbc -pbkdf2 -iter 100000 -salt -in files/451fd69b -k picoCTF
```

**Answer: `picoCTF{trust_but_verify_451fd69b}`**