# IPv6 Attack Defenses

## If you do Not use IPv6 Internally

* disabling IPv6 entirely may cause some side effects, so the best thing to do is...
* block DHCPv6 traffic and incoming router advertisements in Windows Firewall via Group Policy
* \(Inbound\) Core Networking - Dynamic Host Configuration Protocol for IPv6 \(DHCPV6-In\)
* \(Inbound\) Core Networking - Router Advertisement \(ICMPv6-In\)
* \(Outbound\) Core Networking - Dynamic Host Configuration Protocol for IPv6 \(DHCPV6-Out\)

## If WPAD is not in use internally, disable it via Group Policy

* this can be done by disabling the WinHttpAutoProxySvc service

## Relaying to LDAP and LDAPS can only be mitigated by

* enabling both LDAP signing and LDAP channel binding

## Prevent any Impersonation of that User via Delegation

* add Admin Users to Protected Users group or marking them as sensitive and cannot be delegated

