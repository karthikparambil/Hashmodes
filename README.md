#  Hashmode

> Quick Hashcat hash mode lookup right from your terminal or browser.

---

##  About

**Hashmode** is a lightweight utility that lets you instantly look up [Hashcat](https://hashcat.net/hashcat/) hash mode numbers without digging through documentation.  
No more forgetting whether MD5 is `0` or NTLM is `1000` just look it up in seconds.

Available as:
- 🖥️ **Shell Script** - use it directly in your terminal during engagements
- 🌐 **Web UI** - browser-based lookup at your fingertips

🔗 **visit:** [karthikparambil.github.io/hashmode](https://karthikparambil.github.io/hashmode/)

---
### Make the script executable
chmod +x hashmodes.sh
 
### Launch the interactive menu
```
./hashmodes.sh
```
 
Once launched, you'll see an interactive menu. Type a hash name or keyword and it returns the matching Hashcat mode number(s).
 
**Example — looking up MD5:**
```
Enter hash type: md5
 
900   MD4
0     MD5
5100  Half MD5
```
 
**Example — looking up NTLM:**
```
Enter hash type: ntlm
 
1000  NTLM
```
 
**Example — looking up SHA:**
```
Enter hash type: sha
 
100   SHA1
1300  SHA2-224
1400  SHA2-256
10800 SHA2-384
1700  SHA2-512
```
 
Then use the mode number directly with Hashcat:
```bash
hashcat -m 1000 -a 0 hashe.txt wordlist.txt
#           ↑
#      mode from hashmode
```
