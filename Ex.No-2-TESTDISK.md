#  Ex.No.2    TestDisk: Open-Source Data Recovery Tool

## Aim :
To use TestDisk step by step to recover a missing partition and repair a corrupted one.



## 🛠️ Installation
Linux (Debian/Ubuntu): sudo apt-get install testdisk

macOS (Homebrew): brew install testdisk

Windows: Download the executable from the official CGSecurity website.

## Procedure

### 1. Create a Log File
- Launch TestDisk from your terminal or command prompt using sudo testdisk (or testdisk_win.exe on Windows).

- Select the [Create] option to generate a log file of the recovery session. This is helpful for future reference or troubleshooting.
<br>
<br>
<p align="center">
<img width="1104" height="637" alt="Screenshot 2025-09-01 152213" src="https://github.com/user-attachments/assets/df248676-08b1-456d-aaa6-671bdc94eba3" />

</p>
<br>
<br>

### 2. Select the Drive to Analyze
- TestDisk will display a list of all detected storage devices.

- Use the Up/Down arrow keys to highlight the drive that contains your lost data.

<br>
<br>
<p align="center">
<img width="1109" height="638" alt="image" src="https://github.com/user-attachments/assets/d3a39cb8-73d1-42e5-8a15-5d3c4b176af6" />


</p>
<br>
<br>

- Select [Proceed] to move to the next step.

### 3. Choose the Partition Table Type
- TestDisk will automatically suggest the most likely partition table type (e.g., Intel/PC, EFI GPT).

- The default value is usually correct. Confirm the selection by pressing Enter.
<br>
<br>
<p align="center">
<img width="1109" height="639" alt="image" src="https://github.com/user-attachments/assets/5a4d4256-5c8a-452a-a8e5-66be8011084d" />


</p>
<br>
<br>

### 4. Analyze Current Partition Structure
- From the main menu, choose [Analyse] and press Enter.
<br>
<br>
<p align="center">
<img width="1112" height="644" alt="image" src="https://github.com/user-attachments/assets/ccfb85e6-b18d-485b-94a5-c28fe32be9be" />


</p>
<br>
<br>

- This will display the current partition table and check for errors or missing partitions.

### 5. Perform a Quick Search
- After the analysis, you will be prompted to perform a [Quick Search].

<br>
<br>
<p align="center">
<img width="1106" height="638" alt="image" src="https://github.com/user-attachments/assets/9b981db1-7df8-4719-9636-8f50a9ee94a1" />

</p>
<br>
<br>

- Select it and press Enter to scan the drive for lost partitions.

- Once a partition is found, you can press p to list its files. Deleted files and folders often appear in red.

- Press q to return to the search results.

  ### 6. Perform a Deeper Search
- If the Quick Search fails to find your lost partitions, select [Deeper Search].

-<br>
<br>
<p align="center"> 
<img width="1121" height="644" alt="image" src="https://github.com/user-attachments/assets/a458a07b-c749-47dd-ab84-9fa6314b54d2" />


</p>
<br>
<br>

- This process can take a long time, as it scans the entire drive, block by block, to find remnants of partition structures.

- Again, use p to preview files and confirm if a found partition is the one you are looking for.

### 7. Modify Partition Status
- After finding the correct partitions, use the Left/Right arrow keys to set their status.

- Use **Left/Right arrow keys** to change status:  
  - **P**: Primary  
  - ***:** Bootable  
  - **L**: Logical  
  - **D**: Deleted

    <br>
<br>
<p align="center">
<img width="1111" height="641" alt="image" src="https://github.com/user-attachments/assets/c4f782fe-9f8e-4deb-9fee-dfb0cc940e11" />

</p>
<br>
<br>

- Ensure that the partitions you want to recover are marked as Primary or Logical (and not deleted).

### 8. Write the Partition Table
- Once you are confident the partition structure is correct, select [Write] from the menu.

<br>
<br>
<p align="center">
<img width="1110" height="645" alt="image" src="https://github.com/user-attachments/assets/08e9afd2-d5ec-4edb-97cb-d9f15761cc41" />

<br>
<br>

- Confirm the operation by pressing y (for yes). This will write the new partition table to your disk.

<br>
<br>
<p align="center">
  <img width="1124" height="662" alt="image" src="https://github.com/user-attachments/assets/9e461d6c-7769-4cec-b03f-57626708c9d4" />

</p>
<br>
<br>


- WARNING: This is a permanent change. Double-check your selections before writing.

### 9. Recover Files
- If you just need to recover a few files without fixing the partition table, you can do so from the file list (after pressing p).

- Navigate to the folder containing your desired files.

- Use the colon : key to select the files you want to recover.

- Press the uppercase C key to copy the selected file(s).

- Navigate to a safe destination on a different storage device and press uppercase C again to paste.

### 10. Exit and Restart
- Once your task is complete, select [Quit] to exit the program.

- If you wrote a new partition table to the drive, it is recommended to restart your computer to allow the operating system to recognize the changes.
