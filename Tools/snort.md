## Snort

### What it is
**Snort** is an open-source **Network Intrusion Detection System (NIDS)** that monitors network traffic in real-time, detects malicious activities, and generates alerts based on predefined or custom rules. It analyzes packets to identify threats like backdoors, port scans, or exploits.

### Why it is important to this project
Snort is the cornerstone of this lab, enabling detection of simulated attacks like FTP logins, directory traversal on the `192.168.56.0/24` network. Configuring and testing Snort rules showcases cybersecurity skills, including IDS deployment and network traffic analysis, enhancing this portfolio.

### Installation guide
Install Snort on **Ubuntu 24.04 LTS** (`192.168.56.103`):
```bash
sudo apt update
sudo apt upgrade 
sudo apt install snort -y
```

### Snort Setup and Usage

- **Configure `HOME_NET`**:
  - During Snort installation or setup, configure the network to monitor as `192.168.56.0/24`.

- **Download Snort Community Rules**:
  - Visit [snort.org](https://www.snort.org/downloads#rule-downloads) in your web browser.
  - Download the **Community Rules** compatible with your Snort version (e.g., v2.9.x for this project).
  - Extract and move rules to Snort’s rules directory:
   

- **Edit Snort Configuration**:
  - Open the configuration file:
    ```bash
    sudo vim /etc/snort/snort.conf
    ```
  - Set:
    ```
    ipvar HOME_NET 192.168.56.0/24
    ```
  - Uncomment:
    ```
    include $RULE_PATH/local.rules
    ```
  - write and quit

- **Test Configuration**:
  - Verify Snort configuration:
    ```bash
    sudo snort -T -c /etc/snort/snort.conf
    ```

### Basic Use Case
Monitor network traffic and detect attacks:
```bash
sudo snort -A console -q -c /etc/snort/snort.conf -i enp0s3