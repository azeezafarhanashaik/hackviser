
# PowerShell Assessment Report


### 1. Get the real command behind the alias `HoldenManeuver`
**Command Run:**
```powershell
alias HoldenManeuver
```
**Answer:** `Get-Runspace`

---

### 2. How many books are found under `Documents\Books`?
**Commands Run:**
```powershell
cd Administrator\Documents\Books
ls
```
**Answer:** `9`

---

### 3. Cmdlet used to display a list of processes on the system
**Answer:** `Get-Process`

---

### 4. How many services have 'MCRN' in their name?
**Command Run:**
```powershell
Get-Service | Where-Object { $_.Name -like "*MCRN*" } | Measure-Object
```
**Answer:** `5`

---

### 5. How many active users are there in the Active Directory environment?
**Command Run:**
```powershell
Get-ADUser -Filter {Enabled -eq $true} | Measure-Object
```
**Answer:** `10`

---

### 6. Which local group has a description mentioning certificates?
**Command Run:**
```powershell
Get-LocalGroup | Where-Object { $_.Description -match "certificate" }
```
**Answer:** `Cert Publishers`

---

### 7. Command to download files from internet or another computer
**Answer:** `Invoke-WebRequest`

---

### 8. What is the build number of the system?
**Command Run:**
```powershell
(Get-ItemProperty "HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion").CurrentBuild
```
**Answer:** `17763`

---

### 9. What is the HotFixID of the installed update?
**Command Run:**
```powershell
Get-HotFix
```
**Answer:** `KB4464455`

---

### 10. Is Defender running on the server?
**Answer:** `No`

---

### 11. Which user has read-only permission to the file named *Abaddon's Gate*?
**Command Run:**
```powershell
Get-Acl "C:\Users\Administrator\Documents\Books\Abaddon's Gate.txt" | Format-List
```
**Answer:** `c.avasarala`

---
