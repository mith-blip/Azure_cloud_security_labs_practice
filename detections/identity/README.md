# Identity detections

KQL detection rules for Microsoft Entra ID identity threats.
Covers sign-in anomalies, privileged access abuse, Conditional Access
failures, and account manipulation.

## Rules in this folder

| File | Description | Severity | MITRE |
|---|---|---|---|
| entra-signin-monitor.kql | Monitor sign-ins for a specific user | Medium | T1078 |
| pim-activation-audit.kql | PIM activation followed by high-priv action | High | T1078.004, T1098 |
| conditional-access-failure.kql | Repeated CA policy blocks from same IP | Medium | T1110, T1621 |
| new-user-high-privilege-role.kql | New user assigned Owner or Global Admin | High | T1098.003 |

## Data sources required

- `SignInLogs` — Entra ID sign-in events
- `AuditLogs` — Entra ID directory changes
- Microsoft Entra ID data connector enabled in Sentinel

## How to deploy

1. Open Microsoft Sentinel → Logs
2. Paste the KQL query and run it to validate
3. Click "New alert rule" → "Create Microsoft Sentinel alert"
4. Set the schedule, threshold, and severity as noted in each file

## Related MITRE ATT&CK techniques

- [T1078 — Valid Accounts](https://attack.mitre.org/techniques/T1078/)
- [T1078.004 — Cloud Accounts](https://attack.mitre.org/techniques/T1078/004/)
- [T1098 — Account Manipulation](https://attack.mitre.org/techniques/T1098/)
- [T1098.003 — Add Cloud Role](https://attack.mitre.org/techniques/T1098/003/)
- [T1110 — Brute Force](https://attack.mitre.org/techniques/T1110/)
- [T1556 — Modify Authentication Process](https://attack.mitre.org/techniques/T1556/)
- [T1621 — MFA Request Generation](https://attack.mitre.org/techniques/T1621/)
