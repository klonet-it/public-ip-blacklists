# 🛡️ Public IP Blacklists – Auto-Updated

This repository provides a curated and automatically updated set of IP blacklists from well-known public sources.

The goal is to simplify access to threat intelligence data for use in:

- Firewalls
- Intrusion detection/prevention systems
- Abuse detection tools
- Security enrichment pipelines

All files are updated hourly via scheduled GitHub Actions and are generated from a private aggregator repository.

---

## 📆 Available Blacklists

| File name              | Description                                                                                                                                                                                                                                           |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `blacklist_active.txt` | Unified IP blacklist (IP → source mapping), based on active threats. **Built from the following sources**: `ipsum`, `ci_badguys`, `abuseipdb`, `emerging_threats`, `greensnow`, `blocklist_ssh`, `blocklist_bruteforce`, `blocklist_bot`, `binarydefense` |
| `firehol.txt`          | FireHOL Level 1 CIDR list                                                                                                                                                                                                                             |
| `firehol_level2.txt`   | FireHOL Level 2 (more aggressive) CIDR list                                                                                                                                                                                                           |
| `spamhaus_drop.txt`    | Spamhaus DROP IP ranges (CIDR)                                                                                                                                                                                                                        |
| `urlhaus.txt`          | IPs from malware URLs via URLhaus                                                                                                                                                                                                                     |
| `torproject.txt`       | IPs of known TOR exit nodes                                                                                                                                                                                                                           |
| `blocklist_apache.txt` | IPs flagged for web-based scanning and attacks                                                                                                                                                                                                        |
| `threatfox_csv.txt`    | IPs involved in recent botnet C2 activities                                                                                                                                                                                                           |
| `binarydefense.txt`    | IPs collected by Binary Defense honeypots                                                                                                                                                                                                             |

---

## 🔄 Update Schedule

- The blacklists are refreshed **hourly** (respecting source limits like AbuseIPDB)
- Only changed sources are re-processed (based on hash checks)
- All data is version-controlled via Git commits

---

## 🔗 Direct Download (raw)

You can fetch any file using `curl` or `wget`:

```bash
curl -O https://raw.githubusercontent.com/klonet-it/public-ip-blacklists/main/firehol.txt
```bash


## 📬 Contact

Maintained by **Stefano De Nardis**

📧 Email: stefano.denardis@klonet.it  
🌐 Website: [https://www.klonet.it](https://www.klonet.it)

