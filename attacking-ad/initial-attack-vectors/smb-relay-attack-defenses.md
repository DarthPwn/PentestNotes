# SMB Relay Attack Defenses

## Enable SMB Signing on all Devices \(Go to Strategy\)

* pro: completely stops the attack
* con: can cause performance issues with file copies

## Disable NTLM Authentication on Network

* pro: completely stops the attack
* con: if Kerberos stops working, Windows defaults back to NTLM

## Account Tiering

* pro: limits domain admins to specific tasks \(e.g. only log onto servers with need for DA\)
* con: enforcing the policy may be difficult

## Local Admin Restriction

* pro: can prevent a lot of lateral movement
* con: potential increase in the amount of service desk tickets

