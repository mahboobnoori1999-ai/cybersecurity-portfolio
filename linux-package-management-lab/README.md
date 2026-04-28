# Linux Package Management Lab

## Objective
This lab focused on using the APT package manager and sudo privileges in a Linux Bash environment.

The objective was to:
- Verify that APT is installed
- Install and uninstall security applications
- Verify installations
- List installed applications
- Reinstall applications using APT

## Tools Used
- Linux Bash Shell
- APT Package Manager
- sudo
- Suricata
- tcpdump

## Skills Demonstrated
- Linux command-line usage
- Package installation and removal
- Verifying installed applications
- Basic system administration
- Security tool management

---

# Task 1 - Verify APT Installation

Command used:

```bash
apt
```

Result:
Verified that the APT package manager was installed and functioning correctly.

Screenshot:
![APT Check](screenshots/apt-check.png)

---

# Task 2 - Install and Uninstall Suricata

## Install Suricata

```bash
sudo apt install suricata
```

## Verify Installation

```bash
suricata
```

## Uninstall Suricata

```bash
sudo apt remove suricata
```

Result:
Successfully installed, verified, and removed the Suricata intrusion detection application.

Screenshots:
![Install Suricata](screenshots/install-suricata.png)

![Verify Suricata](screenshots/suricata-verify.png)

![Uninstall Suricata](screenshots/uninstall-suricata.png)

---

# Task 3 - Install tcpdump

Command used:

```bash
sudo apt install tcpdump
```

Result:
Successfully installed tcpdump network traffic analysis tool.

Screenshot:
![Install tcpdump](screenshots/install-tcpdump.png)

---

# Task 4 - List Installed Applications

Command used:

```bash
apt list --installed
```

Result:
Verified that tcpdump was installed successfully.

Screenshot:
![Installed Applications](screenshots/apt-installed-list.png)

---

# Task 5 - Reinstall Suricata

Command used:

```bash
sudo apt install suricata
```

Result:
Successfully reinstalled the Suricata application.

Screenshot:
![Reinstall Suricata](screenshots/reinstall-suricata.png)

---

# Key Takeaways

- Learned how to manage software packages in Linux
- Used sudo privileges for administrative tasks
- Installed and removed cybersecurity tools
- Verified software installation status
- Practiced Linux system administration basics
