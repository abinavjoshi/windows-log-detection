# 🛡️ Detection Report: Failed Logon Attempts

**Detection Rule:** Empire Suspicious Failed Logon  
**Log Source:** FailedLogon.evtx  
**Tool Used:** Chainsaw + Sigma  
**Date Analyzed:** June 25, 2025

---

### 🔍 What was detected?

This detection rule looks for multiple failed logon events on a Windows system (Event ID 4625).  
These kinds of log entries often indicate:

- A brute force attack (trying many passwords quickly)
- Password spraying (same password across many usernames)
- Unauthorized access attempts

---

### 📄 Chainsaw Output

The rule was applied using Chainsaw with Sigma and a mapping file.  
Chainsaw scanned the `.evtx` log file, and attempted to match the behavior pattern defined in the rule.

✅ The command used:

```bash
/Users/aj/chainsaw/target/release/chainsaw hunt logs/FailedLogon.evtx \
--sigma sigma_rules/failed_logon.yml \
--mapping mappings/sigma-event-logs-all.yml \
--json > detections/failed_logon.json


