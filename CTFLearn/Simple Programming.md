Can you help me? I need to know how many lines there are where the number of 0's is a multiple of 3 or the numbers of 1s is a multiple of 2. Please! Here is the file: https://mega.nz/#!7aoVEKhK!BAohJ0tfnP7bISIkbADK3qe1yNEkzjHXLKoJoKmqLys

```python
Lines = 0
with open('data.txt', 'r') as file:
    for line in file:
        line = line.strip()  # Remove any leading/trailing whitespaces or newlines
        count_zeros = line.count("0")
        count_ones = line.count("1")
        if count_ones % 2 == 0 or count_zeros % 3 == 0:
            Lines += 1
print(Lines)
```

```bash
python3 main.py
```

![[Captura desde 2024-09-25 00-58-01.png]]

**flag: `6662`**