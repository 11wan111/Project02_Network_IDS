
## Vim

### What it is
**Vim** is a highly efficient, terminal-based text editor for editing configuration files, scripts, and rules. Known for its speed and customizability, it’s a staple in Linux environments like those used in this lab.

### Why it is important to this project
Vim is essential for editing Snort’s configuration (`/etc/snort/snort.conf`) and rule files (`/etc/snort/rules/local.rules`) on Ubuntu. Its lightweight design suits resource-constrained VMs, and proficiency with Vim demonstrates Linux command-line expertise, a valuable skill for this cybersecurity portfolio.

### Installation guide
Install Vim on **Ubuntu 24.04 LTS** and **Kali Linux** using:
```bash
sudo apt update
sudo apt upgrade 
sudo apt install vim -y
```

### Basic Use Case

Edit Snort rules using Vim:
```bash
vim /etc/snort/rules/local.rules
```
**Commands**:
- Enter insert mode: `i`
- Search for a rule: `/` followed by any part of the rule syntax (e.g., `sid:195`)
- Save and exit: `Esc`, `:wq`, `Enter`