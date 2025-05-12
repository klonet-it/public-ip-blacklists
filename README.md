# 🛡️ Public IP Blacklists – Auto-Updated

This repository provides a curated and automatically updated set of IP blacklists from well-known public sources.

The goal is to simplify access to threat intelligence data for use in:

- Firewalls
- Intrusion detection/prevention systems
- Abuse detection tools
- Security enrichment pipelines

All files are updated **daily** via scheduled GitHub Actions and are generated from a private aggregator repository.

---

## 📦 Available Blacklists

| File name               | Description                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| `exported_blacklist.txt` | Unified IP blacklist (IP → source mapping), based on hostile IPs           |
| `firehol.txt`           | [FireHOL Level 1](https://firehol.org/) CIDR list                           |
| `spamhaus_drop.txt`     | [Spamhaus DROP](https://www.spamhaus.org/drop/) IP ranges (CIDR)           |
| `spamhaus_edrop.txt`    | [Spamhaus EDROP](https://www.spamhaus.org/drop/) IP ranges (CIDR, emerging)|
| `urlhaus.txt`           | IPs from malware URLs via [URLhaus](https://urlhaus.abuse.ch/)             |

---

## 🔄 Update Schedule

- The blacklists are refreshed **every day at 03:00 UTC**
- Only changed sources are re-processed
- The data is version-controlled via Git commits

---

## 🔗 Direct Download (raw)

Use `curl` or `wget` to fetch any list directly:

```bash
curl -O https://raw.githubusercontent.com/klonet-it/public-ip-blacklists/main/exported_blacklist.txt


## 🧾 File Format

### `exported_blacklist.txt`

Text format, one IP per line, followed by the sources where that IP appeared:

1.2.3.4 ipsum
5.6.7.8 abuseipdb,blocklist_de

This file allows you to:
- Track which sources listed each IP
- Apply weighted filtering based on source count or trust

### Other `.txt` files

The other files (e.g., `firehol.txt`, `spamhaus_drop.txt`) are plain text files, each containing:
- **One IP or CIDR block per line**
- No comments or metadata
- Ready to use in firewall rules, blocklists, SIEM systems



## 📚 Sources Used

This repository aggregates public IP threat feeds from the following sources:

- 🌐 [Stamparm / Ipsum](https://github.com/stamparm/ipsum) – A curated list of hostile IPs
- 🔒 [CIArmy](https://www.ciarmy.com/) – Community-based list of abusive IPs
- 🚨 [AbuseIPDB](https://www.abuseipdb.com/) – Collaborative IP threat database (API key required)
- 📮 [Blocklist.de](https://www.blocklist.de/) – Brute force and abuse IPs from system logs
- 🧠 [Emerging Threats](https://rules.emergingthreats.net/) – Compromised IPs collected by Proofpoint
- 🧱 [Spamhaus DROP / EDROP](https://www.spamhaus.org/drop/) – Highly abusive IP ranges
- 🔥 [FireHOL Level 1](https://firehol.org/) – Consolidated list of known dangerous IPs
- 🦠 [URLhaus](https://urlhaus.abuse.ch/) – Malware-related IPs extracted from malicious URLs
