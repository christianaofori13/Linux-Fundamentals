# Linux Fundamentals Assignment 🐧

## 📌 Project Overview

This repository documents my **Linux Fundamentals Assignment**, completed as part of the GRC course in the September 2026 cohort. The project focuses on developing foundational Linux command-line skills, inspecting system resources, identifying kernel information, and testing network connectivity using the Kali Linux virtual machine.

The assignment demonstrates practical experience with essential Linux commands and basic networking diagnostics, which are important skills in cybersecurity, system administration, and IT support.

## 👩‍💻 Author Information

- **Name:** Christiana Ofori Ansong
- **Course:** GRC
- **Cohort:** September 2026
- **Assignment Date:** September 25, 2026
- **Operating System:** Kali Linux
- **Project Category:** Linux Fundamentals and Network Diagnostics

## 🎯 Project Objectives

The objectives of this assignment were to:

- Identify the current Linux username, hostname, and working directory.
- Inspect the virtual machine's memory and available disk space.
- Determine the Linux kernel version.
- Test network connectivity using the `ping` command.
- Examine packet transmission, packet loss, and round-trip time.
- Resolve a domain name to an IP address.
- Understand the use of command-line options for network troubleshooting.

## 🛠️ Tools and Technologies

| Tool or Technology | Purpose |
|---|---|
| Kali Linux | Linux operating system used for the practical assignment |
| Linux Terminal | Execute commands and inspect system information |
| `whoami` | Identify the current user |
| `hostname` | Display the system hostname |
| `pwd` | Display the current working directory |
| `free` | Inspect memory usage |
| `df` | Check filesystem disk space |
| `uname` | Retrieve kernel information |
| `ping` | Test network connectivity and measure response times |
| DNS | Resolve domain names to IP addresses |

## 🧪 Practical Tasks and Implementation

### Task 1: Identifying Basic Linux System Information

The first part of the assignment focused on identifying the user's session and the system's current location in the filesystem.

#### Commands

**1. Check the current username**

```bash
whoami
```

The `whoami` command displays the username of the account currently executing commands in the terminal.

**2. Check the hostname**

```bash
hostname
```

The `hostname` command displays the name assigned to the computer or virtual machine.

**3. Check the current working directory**

```bash
pwd
```

The `pwd` command stands for *print working directory*. It displays the absolute path of the directory in which the terminal is currently operating.

#### Expected Learning Outcome

These commands provide a basic understanding of the current Linux session, system identity, and filesystem navigation.

*Note: The assignment PDF does not include the actual output values for the username, hostname, or working directory.*

### Task 2: Inspecting System Resources and Kernel Information

This task involved examining the virtual machine's available memory, disk space, and Linux kernel version.

#### Commands

**1. Check RAM usage**

```bash
free -h
```

The `free -h` command displays memory statistics in a human-readable format, including total, used, free, and available memory.

**2. Check available disk space**

```bash
df -h
```

The `df -h` command displays filesystem disk-space usage in a human-readable format. It helps identify the total space, used space, and remaining space on mounted filesystems.

**3. Check the kernel version**

```bash
uname -r
```

The `uname -r` command displays the release version of the currently running Linux kernel.

#### Results

| System Metric | Recorded Result |
|---|---|
| Total RAM of the virtual machine | 1.9 GiB |
| Available disk space on the main partition | 59 GB |
| Linux kernel version | `6.18.12+kali-amd64` |

#### Analysis

The virtual machine has approximately 1.9 GiB of RAM and 59 GB of available disk space on the main partition, according to the assignment results.

The kernel version identifies the release of the Linux kernel running in the Kali Linux environment. Kernel information is useful when documenting a system, troubleshooting compatibility issues, and understanding the environment used for security testing.

### Task 3: Testing Network Connectivity

The next part of the assignment involved using `ping` to test network connectivity and observe the time taken for packets to travel to a destination and return.

#### Command

```bash
ping -c 2 8.8.8.8
```

The command sends two ICMP echo requests to `8.8.8.8`, a public Google DNS resolver, and then stops.

**Command breakdown:**

- `ping`: Sends network probes to test reachability.
- `-c`: Specifies the number of packets to send before stopping.
- `2`: Sets the number of packets to two.
- `8.8.8.8`: The destination IP address.

#### Results

| Network Metric | Recorded Result |
|---|---|
| Average round-trip time | 13.034 ms |
| Packets sent | 2 |
| Packets received | 2 |
| Packet loss | 0% |

#### Analysis

The recorded average round-trip time was **13.034 milliseconds**, indicating the time taken for the packets to travel to the destination and for the responses to return.

The test recorded 0% packet loss, meaning both transmitted packets received responses. This indicates successful connectivity to the tested destination during the measurement.

However, a successful ping test alone does not establish the overall performance or security of the entire network.

### Task 4: Testing Domain Name Resolution

This task involved pinging `google.com` to observe how a domain name resolves to an IP address and how the destination responds to network probes.

#### Command

```bash
ping -c 4 google.com
```

#### Command breakdown

- `ping`: Tests reachability by sending ICMP echo requests.
- `-c`: Sets a limit on the number of packets sent.
- `4`: Sends four packets before stopping.
- `google.com`: The domain name being tested.

#### Recorded Result

The assignment recorded the following resolved IP address:

```text
192.178.192.139
```

The destination was displayed as:

```text
PING google.com (192.178.192.139)
```

#### Analysis

The output demonstrates that the domain name `google.com` was resolved to an IP address before the ping requests were sent.

The assignment also noted that the response time was similar to the result from pinging `8.8.8.8`, with potential differences arising from routing and server-location differences.

Domain name resolution is an essential networking function because it allows users and applications to access network services using domain names rather than remembering numerical IP addresses.

The `-c 4` option limits the test to four ping packets, after which the command terminates automatically.

## 📊 Summary of Findings

The practical assignment covered Linux system identification, resource inspection, and basic network testing.

| Area | Finding |
|---|---|
| System identification | Practised `whoami`, `hostname`, and `pwd` |
| Memory inspection | 1.9 GiB of total RAM recorded |
| Disk inspection | 59 GB of available space recorded |
| Kernel identification | `6.18.12+kali-amd64` |
| Network connectivity | 13.034 ms average RTT recorded |
| Packet delivery | 2 packets received out of 2 sent |
| Packet loss | 0% recorded |
| DNS resolution | `google.com` resolved to `192.178.192.139` |
| Ping packet count | `-c 4` sends four packets |

## 🔐 Cybersecurity Relevance

The skills practised in this assignment contribute to several areas of cybersecurity and IT operations:

- **Linux administration:** Understanding the user session, hostname, filesystem, and operating environment.
- **System monitoring:** Checking memory and storage resources to assess the system's available capacity.
- **Network troubleshooting:** Using ping responses and packet-loss statistics to investigate connectivity issues.
- **DNS fundamentals:** Understanding how domain names resolve to IP addresses.
- **Technical documentation:** Recording system configurations, commands, and observed results in a structured format.

These foundational skills support more advanced learning in network security, security operations, vulnerability assessment, and incident investigation.

## 💡 Key Lessons Learned

Through this assignment, I practised how to:

1. Use basic Linux commands to identify the active user, hostname, and working directory.
2. Inspect memory, disk-space availability, and kernel information.
3. Interpret ping results, including average round-trip time and packet loss.
4. Understand how the `-c` option controls the number of ping requests.
5. Observe DNS resolution when testing a domain name.
6. Document technical findings in a clear and reproducible manner.

## 🚀 Future Improvements

Building on this exercise, I plan to expand my practical knowledge by exploring:

- Additional Linux commands for system monitoring and administration.
- Network troubleshooting using `ip`, `ip route`, and `traceroute`.
- DNS inspection using tools such as `nslookup` and `dig`.
- Network traffic analysis using Wireshark.
- Linux permissions, users, groups, and access control.
- System logs and security monitoring.
- Practical networking and cybersecurity laboratory exercises.

## 📁 Suggested Repository Structure

```text
linux-fundamentals-assignment/
│
├── README.md
├── Complete Assignment.pdf
└── screenshots/
    ├── system-information.png
    ├── system-resources.png
    └── network-connectivity.png
```

*The
