```bash
file enc_file
cat enc_file
cat enc_file | base64 -d
echo 'd3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX2xoNjBsMDBpfQ==' | base64 -d
```

![[Captura desde 2024-09-04 00-02-36.png]]

![[Captura desde 2024-09-04 00-04-51.png]]

`wpjvJAM{jhlzhy_k3jy9wa3k_lh60l00i}`

```bash
def rot_cipher_decode(text, shift):
    decoded_text = ""
    for char in text:
        if char.isalpha():
            base = ord('A') if char.isupper() else ord('a')
            decoded_text += chr((ord(char) - base - shift) % 26 + base)
        else:
            decoded_text += char
    return decoded_text

def rot47_decode(text):
    decoded_text = ""
    for char in text:
        if 33 <= ord(char) <= 126:
            decoded_text += chr(33 + ((ord(char) - 33 + 47) % 94))
        else:
            decoded_text += char
    return decoded_text

def decode_all_rots(text):
    decoded_versions = {}
    for shift in range(1, 26):
        decoded_versions[f"ROT-{shift:02}"] = rot_cipher_decode(text, shift)
    decoded_versions["ROT-47"] = rot47_decode(text)
    return decoded_versions

def print_decoded_versions(decoded_versions):
    for shift, decoded_text in decoded_versions.items():
        print(f"{shift}: {decoded_text}")

if __name__ == "__main__":
    input_text = input("Enter the text to decode: ")
    decoded_versions = decode_all_rots(input_text)
    print_decoded_versions(decoded_versions)
```

![[Captura desde 2024-09-04 00-07-42.png]]

**flag `picoCTF{caesar_d3cr9pt3d_ea60e00b}`**