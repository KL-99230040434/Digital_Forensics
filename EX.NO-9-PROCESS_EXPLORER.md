## 🕵️ Ex.No.9: Analyzing Suspicious Processes with Process Explorer 🖥️

**Overview**  
**Process Explorer** is a powerful Windows tool that provides detailed insights into running processes. It helps monitor system activity, troubleshoot issues, and detect potentially malicious or unusual processes. 🔍

---

### Step 1: Download and Launch Process Explorer ⬇️

* **Get Process Explorer:**  
  Visit the Microsoft Sysinternals website and download the tool. 🌐
* **Extract Files:**  
  Unzip the downloaded package into a dedicated folder. 📂
* **Run as Administrator:**  
  Open the folder and launch `procexp64.exe` or `procexp.exe` by right-clicking and selecting **Run as Administrator**. 🛡️

![WhatsApp Image 2025-10-27 at 22 44 22_00b6e52c](https://github.com/user-attachments/assets/8661068e-c436-431d-968e-d1331235f0a0)


---

### Step 2: Explore the Interface 🖱️

Process Explorer displays processes in a hierarchical tree structure. Each process is **color-coded** based on its status:

| Color | Description |
| :--- | :--- |
| **Pink** | Suspended processes ⏸️ |
| **Light Blue** | Processes running under your account 👤 |
| **Dark Blue** | System services or processes 🖥️ |
| **Green** | Newly started processes 🟢 |
| **Red** | Recently terminated processes ❌ |

---

### Step 3: Spotting Suspicious Processes ⚠️

To investigate potentially harmful processes:

1. **Check Unknown Processes:**  
   Look for unfamiliar names. Trusted processes usually come from known vendors like Microsoft, Adobe, or Intel. ✅
2. **Verify Digital Signatures:**  
   Right-click → **Properties** → **Image** tab. Check for a valid **Digital Signature**. Unsigned processes may be risky. 🛑
3. **Examine File Paths:**  
   Check the **Path** under the Image tab. Legitimate system processes are usually in `C:\Windows\System32`. Running from temp or user folders is suspicious. 📁
4. **Monitor Resource Usage:**  
   Watch for processes consuming excessive CPU, memory, or disk resources without explanation. 💻
5. **Review Process Details:**  
   Lack of description or unclear company names can indicate a suspicious process. 🕵️‍♂️
6. **Inspect Network Activity:**  
   Right-click → **Properties** → **TCP/IP** tab. Unexpected external connections require attention. 🌐

---
![WhatsApp Image 2025-10-27 at 22 51 03_d11577cb](https://github.com/user-attachments/assets/1bcd2218-c116-4f97-af68-fe12534dbd2c)


### Step 4: Research Suspicious Processes 🔎

* Search the process name online (e.g., `cmd.exe`) to learn more about it. 🌍  
* Use databases like **VirusTotal** or **ProcessLibrary** to check for known malware. 🦠


<img width="921" height="995" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/7242c70c-2370-4495-ad2c-4d8f9dc7ebbf" />


---

### Step 5: Handle Malicious or Unwanted Processes 🛠️

* **Terminate:** Right-click → **Kill Process** to stop it immediately. ❌  
* **Suspend:** Right-click → **Suspend** to pause execution temporarily. ⏸️  
* **Delete Source:** Locate the executable via its Path and remove it if confirmed malicious. 🗑️

---
<img width="971" height="550" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/5d29ce2e-7963-4294-b235-fa1684931717" />



---

### Step 6: Conduct a Full System Scan 🧹

* Run a comprehensive antivirus scan. 🛡️  
* Use malware removal tools (e.g., Malwarebytes or Windows Defender) for a thorough cleanup. 🧰
