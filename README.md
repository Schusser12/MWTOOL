# 🛡️ Merged Malware Look-up Tool (`merged_mwtool`)

Bash function for investigating quarantined malware files across both site and user scopes.

---

## 🚀 Features

- **Date-based filtering** (e.g., last `N` days)
- **Per-user** and **per-domain** quarantine analysis
-  **Malware signature inspection**:
  - HEX pattern analysis (with ASCII translation)
  - YARA rule insights
  -  CAV/ClamAV detection results (e.g., `Win.Trojan.Remcos`, `Win.Dropper.NetWire`, etc.)
- Smart **deduplication** between site and user findings
- Auto-generated timestamped reports

---

## 🛠️ Usage

```bash
merged_mwtool [options]
```

### Options:

| Option       | Description                                  |
|--------------|----------------------------------------------|
| `-d, --days` | Number of days to look back in logs          |
| `-h, --help` | Display usage instructions                   |

Example:
```bash
merged_mwtool --days 7
```

---

## 📂 Output

Generates a timestamped text report in your home directory:
```
~/merged_mwtool-04-24-25T14:32.txt
```
