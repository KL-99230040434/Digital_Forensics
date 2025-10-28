# 🕵️‍♂️ **Experiment No. 06 — Digital Forensic Analysis using Sleuth Kit (TSK)**

## 🔍 **Overview**

The **Sleuth Kit (TSK)** 🧰 is a versatile suite of command-line tools used in **digital forensics**.  
It enables investigators to analyze disk images 🖥️, uncover deleted files 🗑️, and extract critical digital evidence 🔎 from storage devices.  
This document walks through the complete process of using Sleuth Kit on a **Windows** system to perform forensic analysis.

---

## ⚙️ **Step 1: Installing Sleuth Kit**

1. **Download the Tool:**  
   - Head over to the official Sleuth Kit page or use this link:  
     👉 [Download Sleuth Kit](https://drive.google.com/drive/u/1/folders/1ilSFY7Tqn2L7AjQGhq8yJ8kixc_xTU-v)  
   - Choose the latest stable **Windows-compatible** version.

2. **Installation Process:**  
   - Run the installer and follow the setup wizard 🪄.  
   - Once done, TSK will be ready to use on your system!

---

## 💾 **Step 2: Acquire the Disk Image**

Before analysis, a **forensic disk image** (a perfect bit-by-bit copy) of the device is needed.

1. **Create Disk Image:**  
   - Use tools like **FTK Imager** 🧮 or **`dd`** to create an exact copy.  
   - Save it in a TSK-supported format: `.dd`, `.raw`, `.img`, or `.E01`.

2. **Sample Evidence Files:**  
   - For this lab, download the following from the provided link:  
     📁 `4Dell Latitude CPi.E01`  
     📁 `4Dell Latitude CPi.E02`

---

## 💽 **Step 3: Mounting the Disk Image (Optional)**

Mounting lets you access the disk image as if it were a normal drive.

- Use **OSFMount** 🧷 to mount the image in **read-only mode**.  
- 🔒 *Note: This is optional but helps when browsing the file system.*

---

## 🧭 **Step 4: File System Analysis with TSK**

Now let’s dive into Sleuth Kit tools 🧠 to inspect the file system.

### 🧑‍💻 Navigate to the TSK Directory

```bash
cd "C:\Program Files (x86)\sleuthkit-4.14.0-win32\bin"
```
📸  
<img width="1477" height="507" alt="image" src="https://github.com/user-attachments/assets/e4f1737d-1304-495e-95f6-f0a4ac926629" />


---

### 🔍 Identify File System Type

```bash
.\fsstat.exe -o 63 "C:\Users\swapn\OneDrive\Downloads\4Dell Latitude CPi.E01"
```
🧾  
<img width="1866" height="776" alt="image" src="https://github.com/user-attachments/assets/5f998f63-adb8-4716-a197-46818a402733" />


💡 *Displays key details about the file system type and structure.*

---

### 🧩 View Partition Layout

```bash
.\mmls.exe "C:\Users\swapn\OneDrive\Downloads\4Dell Latitude CPi.E01"

```
📊  
<img width="1919" height="196" alt="image" src="https://github.com/user-attachments/assets/22f93f7f-2ecb-4f6d-a322-d4ea06548c6e" />



➡️ *Lists all partitions and their respective start/end addresses.*

---

### 📂 List Files and Directories

```bash
.\fls.exe -o 63 "C:\Users\swapn\OneDrive\Downloads\4Dell Latitude CPi.E01"

```
🧾  
<img width="1918" height="779" alt="image" src="https://github.com/user-attachments/assets/45e57527-1dbf-487b-9fe3-d409f2b726db" />



🔸 *Recursively lists files and folders with their inode details.*

---

### 🗃️ Recover Deleted Files

```bash
.\icat.exe -o 63 "C:\Users\swapn\Downloads\4Dell Latitude CPi (1).E01" 119 >"C:\Users\swapn\Downloads\BOOTLOG_recovered.TXT"
```
🖼️  
<img width="1915" height="83" alt="image" src="https://github.com/user-attachments/assets/9fe20f42-7fd6-4ae1-bbd4-a191db0a9c18" />



💾 *Recovers a deleted or existing file by its inode number.*

---

## 🕰️ **Step 5: Metadata Analysis**

To uncover file history and access details, view the file’s metadata.
🖼️ 
<img width="1919" height="981" alt="image" src="https://github.com/user-attachments/assets/29429b46-8389-4a13-b78d-e021daeb44c6" />

```bash
.\istat.exe -o 63  "C:\Users\swapn\Downloads\4Dell Latitude CPi (1).E01" 119 >"C:\Users\swapn\Downloads\BOOTLOG_recovered.TXT"



---
📘 *Displays file attributes such as MAC times (Modified, Accessed, Changed), size, and allocation info.*

---


## 📜 **Step 6: Report Generation**

After completing your analysis:

1. **Compile All Outputs:**  
   Collect files like `filesystem_info.txt`, `partitions.txt`, `file_list.txt`, and `timeline.txt`.

2. **Interpret and Document:**  
   Write a clear summary 📑 explaining your findings, methods used, and any key recovered evidence.

---

## 🔐 **Step 7: Evidence Preservation**

Ensuring the integrity of evidence is the final and most important step 🧳.

1. **Archive Evidence Securely:**  
   Use encryption 🔒 and hashing 🧮 to store your disk image and findings.

2. **Maintain Chain of Custody:**  
   Keep the evidence in a secure location following proper forensic protocols ⚖️.

---

## ✅ **Conclusion**

Using the **Sleuth Kit (TSK)**, investigators can efficiently extract, analyze, and preserve digital evidence 💾.  
It remains one of the most reliable and open-source forensic toolkits for digital investigation 🚔.
