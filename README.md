# PCMan_FTP_Server_2_07_STOR_Remote_Buffer_Overflow
A buffer overflow is triggered when a long STOR command is sent to the server continued of these  /../ parameters 
# PCMan FTP Server 2.07 - 'STOR' Remote Buffer Overflow (Remote Code Execution)

## 📅 Date
March 1, 2013

## ✍️ Exploit Author
- **Christian (Polunchis) Ramirez** — [https://intlabs.ca](https://intlabs.ca)

**Contacts:**  
- polunchis@intlabs.ca  


## 📦 Software Information
- **Affected Software:** PCMan FTP Server 2.07
- **Vendor Website:** *(Vendor website appears inactive)*
- **Vulnerability Type:** Remote Buffer Overflow (Remote Code Execution)

## 🖥️ Tested On
- Windows XP SP3 (English)

## 🛡️ Vulnerability Description
A **remote buffer overflow vulnerability** exists in **PCMan FTP Server 2.07**.  
When a maliciously crafted `STOR` FTP command is sent to the server, it improperly handles user input, allowing an attacker to **overwrite the Instruction Pointer (EIP)** and execute arbitrary code on the target machine.

**No authentication** is required to exploit this vulnerability.

This flaw allows **full remote code execution** with the privileges of the user running the PCMan FTP service.

## ⚙️ Exploitation Details
- **Port:** 21/TCP (FTP)
- **Command:** `STOR`
- **Attack Vector:** Remote
- **Authentication:** Not required
- **Impact:** Full remote code execution

## 🛠️ Usage
⚠️ **Warning:**  
This exploit is for educational and authorized penetration testing purposes only. Unauthorized access to systems without permission is illegal.

```bash
# Example usage (if you provide exploit.py)
python exploit.py --target <IP_ADDRESS> --port 21
