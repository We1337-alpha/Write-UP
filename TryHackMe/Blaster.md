possible to use `nc` but is very slow

```bash
nc -zv 0.0.0.0 1-1000
```

```python
import socket
import time


def scanner(ip, port):
    try:
        sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
        sock.settimeout(0.5)
        sock.connect((ip, port))
        print(f"[!] Port {port} is open")
    except socket.timeout:
        pass
    except socket.error:
        pass
    finally:
        sock.close()


def main():
    try:
        ip_addr = input("[~] Enter the IP address to scan: ")
        port_range = input("[~] Enter port range (separated by a comma ','): ").split(',')
        port_start = int(port_range[0])
        port_end = int(port_range[1])

        if port_start > port_end or port_start < 1 or port_end > 65535:
            raise ValueError("Invalid port range. Ports must be between 1 and 65535.")
        
        print(f"[~] Scanning {ip_addr} from port {port_start} to {port_end}...")

        start_time = time.time()
        for port in range(port_start, port_end + 1):
            scanner(ip_addr, port)
        end_time = time.time()

        print(f"\n[~] Scan completed in {end_time - start_time:.2f} seconds.")
        
    except ValueError as ve:
        print(f"[!] Error: {ve}")
    except Exception as e:
        print(f"[!] Unexpected error: {e}")


if __name__ == "__main__":
    main()
```



```bash
ffuf -u http://10.10.209.143/FUZZ -w /home/usuario/Descargas/SecLists-master/Discovery/Web-Content/big.txt
```

![[Captura desde 2024-09-16 00-54-30.png]]

