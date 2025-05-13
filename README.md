🛡️ Public IP Blacklists – Auto-Updated

This repository provides a curated and automatically updated set of IP blacklists from well-known public sources.

The goal is to simplify access to threat intelligence data for use in:

Firewalls

Intrusion detection/prevention systems

Abuse detection tools

Security enrichment pipelines

All files are updated daily via scheduled GitHub Actions and are generated from a private aggregator repository.

📆 Available Blacklists

File name

Description

blacklist_active.txt

Unified IP blacklist (IP → source mapping), based on active threats. Built from the following sources: ipsum, ci_badguys, abuseipdb, emerging_threats, greensnow, blocklist_ssh, blocklist_bruteforce, blocklist_bot, binarydefense

firehol.txt

FireHOL Level 1 CIDR list

firehol_level2.txt

FireHOL Level 2 (more aggressive) CIDR list

spamhaus_drop.txt

Spamhaus DROP IP ranges (CIDR)

urlhaus.txt

IPs from malware URLs via URLhaus

torproject.txt

IPs of known TOR exit nodes

blocklist_apache.txt

IPs flagged for web-based scanning and attacks

threatfox_csv.txt

IPs involved in recent botnet C2 activities

binarydefense.txt

IPs collected by Binary Defense honeypots

🔄 Update Schedule

The blacklists are refreshed hourly (respecting source limits like AbuseIPDB)

Only changed sources are re-processed (based on hash checks)

All data is version-controlled via Git commits

🔗 Direct Download (raw)

You can fetch any file using curl or wget:

curl -O https://raw.githubusercontent.com/klonet-it/public-ip-blacklists/main/firehol.txt

Or clone the repository:

git clone https://github.com/klonet-it/public-ip-blacklists.git

📌 File Format

blacklist_active.txt

Text format: one IP per line, followed by the source(s) where that IP appeared:

1.2.3.4 ipsum
5.6.7.8 abuseipdb,blocklist_ssh

This file allows you to:

Track which source(s) flagged each IP

Apply filtering or scoring based on source trust level

Other .txt files

Each .txt file (like firehol.txt, urlhaus.txt) is:

One IP or CIDR block per line

No metadata or headers

Ready for ingestion into firewalls, proxies, IDS/IPS, or enrichment pipelines

📒 Sources Used

This repository aggregates public IP threat feeds from:

🌐 Stamparm / Ipsum

🔐 CIArmy

⚠️ AbuseIPDB

📨 Blocklist.de

🧠 Emerging Threats

🛡️ Spamhaus DROP

🔥 FireHOL Level 1/2

🦠 URLhaus

🕵️‍♂️ Tor Project

💡 BinaryDefense

🪡 ThreatFox

📄 License

This repository is released under the MIT License.

You are free to:

Use the data in personal, commercial, or research projects

Redistribute or integrate it in other systems

Modify or extend the files

Please retain attribution where applicable and respect the original data source licenses when redistributing.

📨 Contact

Maintained by Stefano De Nardis


## 📬 Contact

Maintained by **Stefano De Nardis**

📧 Email: stefano.denardis@klonet.it  
🌐 Website: [https://www.klonet.it](https://www.klonet.it)

