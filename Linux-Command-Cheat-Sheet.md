
# Linux Command Cheat Sheet

A quick reference to Linux commands practised during Task 1 of the ApexPlanet Cybersecurity Internship.

## 1. Directory and File Operations

| Command |          Purpose              |          Example           |
|---------|-------------------------------|----------------------------|
| `pwd`   | Display the current directory | `pwd`                      |
| `ls`    | List files and directories    | `ls -l`                    |
| `mkdir` | Create a directory            | `mkdir EHF_Practical`      |
| `cd`    | Change directory              | `cd EHF_Practical`         |
| `touch` | Create an empty file          | `touch evidence.txt`       |
| `cat`   | Display file contents         | `cat evidence.txt`         |
| `cp`    | Copy a file                   | `cp evidence.txt copy.txt` |
| `mv`    | Rename or move a file         | `mv copy.txt renamed.txt`  |
| `rm`    | Remove a file                 | `rm filename.txt`          |

## 2. File Permissions

| Command |         Purpose         |         Example          |
|---------|-------------------------|--------------------------|
| `ls -l` | View file permissions   | `ls -l evidence.txt`     |
| `chmod` | Change file permissions | `chmod 644 evidence.txt` |

Permission values:
- `4` = Read
- `2` = Write
- `1` = Execute
- `7` = Read, write, and execute

For example, `chmod 644 evidence.txt` gives the owner read/write permission and gives the group and others read permission.

## 3. Network Inspection

|        Command        |                  Purpose                    |
|-----------------------|---------------------------------------------|
| `ip -br addr`         | Display network interfaces and IP addresses |
| `ip route`            | Display routing information                 |
| `ping 192.168.56.101` | Test connectivity to the lab target         |
| `ss -tuln`            | Display listening TCP and UDP sockets       |

## 4. Cryptography with OpenSSL

|      Command      |              Purpose                |
|-------------------|-------------------------------------|
| `openssl version` | Check the installed OpenSSL version |
| `openssl help`    | Display OpenSSL command help        |

OpenSSL can also encrypt and decrypt sample files. Use the commands and options appropriate to the encryption method used in your lab.

## 5. Packet Analysis with Wireshark

- Select the correct network interface before starting a capture.
- Generate test traffic in the controlled lab.
- Use the display filter `icmp` to show ICMP packets.
- Inspect packet details to understand the captured traffic.
- Save captures in `.pcapng` format for later analysis.

## 6. Cybersecurity Tool Checks

|    Tool    |                  Purpose                     |
|------------|----------------------------------------------|
| Nmap       | Network discovery and port scanning          |
| Burp Suite | Web application security testing             |
| Netcat     | Network connection and data-transfer utility |
| OpenSSL    | Cryptographic operations                     |

## 7. Lab Safety
- Perform testing only on systems you own or are authorized to examine.
- Keep intentionally vulnerable virtual machines isolated on a Host-Only network.
- Avoid exposing vulnerable lab machines to public or untrusted networks.
- Do not publish passwords, private keys, or sensitive packet captures.
