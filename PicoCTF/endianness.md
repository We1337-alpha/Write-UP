```bash
nc titan.picoctf.net 58151
```
 
little endianness and big endianness representation how data stored in memory, bytes begins from first to last or last to first

https://en.wikipedia.org/wiki/Endianness

![[Captura desde 2024-09-04 00-34-05.png]]

example `pubjm` hex representation will be `7075626A6D`:

![[Captura desde 2024-09-04 00-48-59.png]]

little endianness `6D6A627570` -> jmbup
big endianness `7075626A6D` -> pubmj

![[Captura desde 2024-09-04 00-35-22.png]]

**flag: `picoCTF{3ndi4n_sw4p_su33ess_91bc76a4}`**