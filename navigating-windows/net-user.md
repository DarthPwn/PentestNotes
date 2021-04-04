# net user

## Overview

* add user accounts

## Add Users to Non-Admin Group

```text
net user username /add
```

```text
net user username password /add
```

```text
net user /add username password
```

## Add User to Administrator Group

```text
net localgroup administrators username /add
```

## Check if You are Part of a Domain

```text
net localgroup /domain
```

## List all Users in a Domain

```text
net users /domain
```

