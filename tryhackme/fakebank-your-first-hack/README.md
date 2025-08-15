# TryHackMe – FakeBank: Your First Hack

**Date Completed:** 2025-08-15  
**Difficulty:** Beginner  
**Category:** Web Exploitation / Enumeration

---

## Objectives
- Enumerate hidden pages with `dirb` and find sensitive functionality.
- Use the discovered endpoint to change account balance.

## Environment
- THM AttackBox (Firefox + dirb)  
- Wordlist: `/usr/share/dirb/wordlists/common.txt`

## Enumeration
```bash
dirb http://fakebank.thm
```
**Results**  
- `http://fakebank.thm/bank-deposit` (200)  
- `http://fakebank.thm/images` (301)

## Exploitation
- Opened `http://fakebank.thm/bank-deposit`
- Deposited `$2000` to account `8881` via the admin portal UI.

## Proof
- Balance updated and a popup displayed the success message (flag provided by the room).  
  Add screenshots to: `assets/screenshots/thm-fakebank/` and reference them like:
```
![dirb](../../assets/screenshots/thm-fakebank/dirb-output.png)
![flag](../../assets/screenshots/thm-fakebank/flag-popup.png)
```

## Remediation Ideas
- Enforce authentication/authorization on administrative endpoints.
- Remove sensitive endpoints from production or gate them behind proper access controls.
- Disable directory/endpoint guessability with obscure paths alone (defense-in-depth).

## Key Takeaways
- Directory brute forcing quickly reveals hidden functionality.
- Never trust client-side visibility to protect admin features.
