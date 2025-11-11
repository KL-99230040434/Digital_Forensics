# END SEM PRACTICAL MHA (Mail Header Analyzer)
# Email Analysis Using MXToolbox
# Mail Header Analyzer (MHA) — Simple Forensic Tool

**Aim:** To examine an email header using a Mail Header Analyzer (MHA) tool in order to trace the origin of the email, check its authenticity, and detect any signs of email spoofing or tampering.

## Files
- `header_analyzer.py` — main script (Python 3.8+)
- `sample_header.txt` — sample raw header (replace with your own)
- `requirements.txt` — Python dependencies

## Setup
1. Create virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate   # Linux/macOS
   venv\Scripts\activate      # Windows

---
# Steps 

# 🧾 Email Header Forensic Analysis (30 Marks)

### 🎯 **Purpose (in Simple Words)**
- To find where an email was actually sent from.  
- To verify if the email is real or fake using its header.  
- To check SPF, DKIM, and DMARC to know if it’s trustworthy.

---

## 🔬 **Forensic Investigation Flow (30 Marks)**

### **Step 1 – Collect the Email Header**
- Open the received email → Click **Show Original Message** or **View Source**.  
- Copy the complete **raw email header** text.
  <img width="1910" height="970" alt="Screenshot 2025-11-11 131604" src="https://github.com/user-attachments/assets/0640f7e5-ee45-49b3-aff8-635749240a0b" />
  <img width="1427" height="771" alt="Screenshot 2025-11-11 131652" src="https://github.com/user-attachments/assets/4be9967b-3107-4a21-86a0-edd6f670a1a7" />



### **Step 2 – Load Header into MHA Tool**
- Open [MXToolbox Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx).  
- Paste the copied header → Click **Analyze Header**.
  <img width="1850" height="936" alt="image" src="https://github.com/user-attachments/assets/b830aefe-e4e3-42c6-a576-9972f6413e93" />
  <img width="1918" height="807" alt="Screenshot 2025-11-11 131746" src="https://github.com/user-attachments/assets/67369160-d34b-407f-9620-88ac83080066" />
  <img width="1889" height="884" alt="Screenshot 2025-11-11 131916" src="https://github.com/user-attachments/assets/da4194b9-e1f0-4acb-8c4e-da69978aaa56" />


### **Step 3 – Identify Email Source**
- In the analysis, find the **“Received”** lines.  
- Identify the **real sender’s IP**, **mail server**, and **country**.
  <img width="1910" height="728" alt="Screenshot 2025-11-11 132042" src="https://github.com/user-attachments/assets/dd032109-df6f-4f47-b3ce-615f103dfe06" />
<img width="1903" height="778" alt="Screenshot 2025-11-11 132142" src="https://github.com/user-attachments/assets/2f88d36f-f4af-45aa-8432-044a8abd1fce" />

### **Step 4 – Check Authentication Results**
- **SPF:** Confirms if sender’s IP is authorized.  
- **DKIM:** Checks if the message was digitally signed.  
- **DMARC:** Ensures SPF/DKIM align with domain policy.
  <img width="1919" height="917" alt="Screenshot 2025-11-11 132234" src="https://github.com/user-attachments/assets/61fab3f4-115b-4afc-966e-7bfdc93668a3" />
  <img width="1916" height="862" alt="Screenshot 2025-11-11 132301" src="https://github.com/user-attachments/assets/d271fd4d-dd1f-4684-a8d5-8c1fac555406" />




### **Step 5 – Analyze Suspicious Elements**
- Look for **fail** in SPF/DKIM/DMARC.  
- Check mismatch between **From** and **sending server**.  
- Detect unusual routing or unknown IP addresses.
  <img width="1886" height="820" alt="Screenshot 2025-11-11 132347" src="https://github.com/user-attachments/assets/f48d2666-ba82-483a-8e3c-e28b28544620" />
  


### **Step 6 – Generate Findings**
- Summarize whether the email is **genuine** or **spoofed**.  
- Explain with reason (e.g., SPF fail, invalid DKIM).

### **Step 7 – Conclusion**
- If SPF, DKIM, and DMARC **pass → authentic email**.  
- If any **fail → suspicious or spoofed email**.
  <img width="1890" height="498" alt="Screenshot 2025-11-11 132503" src="https://github.com/user-attachments/assets/5401156b-142d-4079-a0fd-b77fa0108d09" />


---

## 🧰 Tools Used
| Tool / Library | Purpose |
|-----------------|----------|
| **pyspf** | SPF record verification |
| **dkimpy** | DKIM signature validation |
| **dnspython** | DMARC policy lookup |
| **email** | Parse email structure |

---

## ⚙️ How to Run
1. Save the full email (raw headers + body) as `message.eml`.  
2. Run the program:  
   ```bash
   python email_forensic.py message.eml

## Results
<img width="1919" height="917" alt="Screenshot 2025-11-11 132234" src="https://github.com/user-attachments/assets/98689df4-0c27-4b6b-8ed1-2546204ad36d" />
<img width="1916" height="862" alt="Screenshot 2025-11-11 132301" src="https://github.com/user-attachments/assets/ade9625e-fb6d-4262-8dbd-92ca40ea0182" />
<img width="1886" height="820" alt="Screenshot 2025-11-11 132347" src="https://github.com/user-attachments/assets/b0b792c6-31c1-4729-be90-46417e8858dd" />


---
## 📌 Features
- Extract & analyze email headers  
- SPF / DKIM / DMARC validation  
- MX & DNS lookups  
- IP blacklist & reputation checks  
- URL extraction  
- MXToolbox API (optional)  
- Automated Python scripts  
# END SEM PRACTICAL MHA (Mail Header Analyzer)
# Email Analysis Using MXToolbox
# Mail Header Analyzer (MHA) — Simple Forensic Tool

**Aim:** To examine an email header using a Mail Header Analyzer (MHA) tool in order to trace the origin of the email, check its authenticity, and detect any signs of email spoofing or tampering.

## Files
- `header_analyzer.py` — main script (Python 3.8+)
- `sample_header.txt` — sample raw header (replace with your own)
- `requirements.txt` — Python dependencies

## Setup
1. Create virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate   # Linux/macOS
   venv\Scripts\activate      # Windows

---
# Steps 

# 🧾 Email Header Forensic Analysis (30 Marks)

### 🎯 **Purpose (in Simple Words)**
- To find where an email was actually sent from.  
- To verify if the email is real or fake using its header.  
- To check SPF, DKIM, and DMARC to know if it’s trustworthy.

---

## 🔬 **Forensic Investigation Flow (30 Marks)**

### **Step 1 – Collect the Email Header**
- Open the received email → Click **Show Original Message** or **View Source**.  
- Copy the complete **raw email header** text.
  <img width="1910" height="970" alt="Screenshot 2025-11-11 131604" src="https://github.com/user-attachments/assets/0640f7e5-ee45-49b3-aff8-635749240a0b" />
  <img width="1427" height="771" alt="Screenshot 2025-11-11 131652" src="https://github.com/user-attachments/assets/4be9967b-3107-4a21-86a0-edd6f670a1a7" />



### **Step 2 – Load Header into MHA Tool**
- Open [MXToolbox Header Analyzer](https://mxtoolbox.com/EmailHeaders.aspx).  
- Paste the copied header → Click **Analyze Header**.
  <img width="1850" height="936" alt="image" src="https://github.com/user-attachments/assets/b830aefe-e4e3-42c6-a576-9972f6413e93" />
  <img width="1918" height="807" alt="Screenshot 2025-11-11 131746" src="https://github.com/user-attachments/assets/67369160-d34b-407f-9620-88ac83080066" />
  <img width="1889" height="884" alt="Screenshot 2025-11-11 131916" src="https://github.com/user-attachments/assets/da4194b9-e1f0-4acb-8c4e-da69978aaa56" />


### **Step 3 – Identify Email Source**
- In the analysis, find the **“Received”** lines.  
- Identify the **real sender’s IP**, **mail server**, and **country**.
  <img width="1910" height="728" alt="Screenshot 2025-11-11 132042" src="https://github.com/user-attachments/assets/dd032109-df6f-4f47-b3ce-615f103dfe06" />
<img width="1903" height="778" alt="Screenshot 2025-11-11 132142" src="https://github.com/user-attachments/assets/2f88d36f-f4af-45aa-8432-044a8abd1fce" />

### **Step 4 – Check Authentication Results**
- **SPF:** Confirms if sender’s IP is authorized.  
- **DKIM:** Checks if the message was digitally signed.  
- **DMARC:** Ensures SPF/DKIM align with domain policy.
  <img width="1919" height="917" alt="Screenshot 2025-11-11 132234" src="https://github.com/user-attachments/assets/61fab3f4-115b-4afc-966e-7bfdc93668a3" />
  <img width="1916" height="862" alt="Screenshot 2025-11-11 132301" src="https://github.com/user-attachments/assets/d271fd4d-dd1f-4684-a8d5-8c1fac555406" />




### **Step 5 – Analyze Suspicious Elements**
- Look for **fail** in SPF/DKIM/DMARC.  
- Check mismatch between **From** and **sending server**.  
- Detect unusual routing or unknown IP addresses.
  <img width="1886" height="820" alt="Screenshot 2025-11-11 132347" src="https://github.com/user-attachments/assets/f48d2666-ba82-483a-8e3c-e28b28544620" />
  


### **Step 6 – Generate Findings**
- Summarize whether the email is **genuine** or **spoofed**.  
- Explain with reason (e.g., SPF fail, invalid DKIM).

### **Step 7 – Conclusion**
- If SPF, DKIM, and DMARC **pass → authentic email**.  
- If any **fail → suspicious or spoofed email**.
  <img width="1890" height="498" alt="Screenshot 2025-11-11 132503" src="https://github.com/user-attachments/assets/5401156b-142d-4079-a0fd-b77fa0108d09" />


---

## 🧰 Tools Used
| Tool / Library | Purpose |
|-----------------|----------|
| **pyspf** | SPF record verification |
| **dkimpy** | DKIM signature validation |
| **dnspython** | DMARC policy lookup |
| **email** | Parse email structure |

---

## ⚙️ How to Run
1. Save the full email (raw headers + body) as `message.eml`.  
2. Run the program:  
   ```bash
   python email_forensic.py message.eml

## Results
<img width="1919" height="917" alt="Screenshot 2025-11-11 132234" src="https://github.com/user-attachments/assets/98689df4-0c27-4b6b-8ed1-2546204ad36d" />
<img width="1916" height="862" alt="Screenshot 2025-11-11 132301" src="https://github.com/user-attachments/assets/ade9625e-fb6d-4262-8dbd-92ca40ea0182" />
<img width="1886" height="820" alt="Screenshot 2025-11-11 132347" src="https://github.com/user-attachments/assets/b0b792c6-31c1-4729-be90-46417e8858dd" />


---
## 📌 Features
- Extract & analyze email headers  
- SPF / DKIM / DMARC validation  
- MX & DNS lookups  
- IP blacklist & reputation checks  
- URL extraction  
- MXToolbox API (optional)  
- Automated Python scripts  

---
## 🧩 Conclusion
In this digital forensic investigation, we examined an email header to identify the source and verify its authenticity.  
By using **SPF**, **DKIM**, and **DMARC** checks, investigators can detect spoofing and confirm whether an email truly came from its claimed sender.

✅ **Authentic Email:** All checks pass (SPF, DKIM, DMARC).  
⚠️ **Spoofed Email:** Any check fails or sender mismatch is found.
---
