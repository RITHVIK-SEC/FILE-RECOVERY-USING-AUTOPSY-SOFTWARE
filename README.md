# FILE-RECOVERY-USING-AUTOPSY-SOFTWARE

## AIM
To use **Autopsy Digital Forensics Tool** to retrieve deleted files from a disk image.

---

## REQUIREMENTS
- **Operating System**: Windows 10/11, macOS, or Linux
- **Tool**: [Autopsy Digital Forensics](https://www.autopsy.com/)  
- **Test Data**: Disk image file (`disk.dd`, `disk.img`, `.E01`)

---

## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Install Autopsy]
    B --> C[Create New Case in Autopsy]
    C --> D[Add Data Source: Disk Image]
    D --> E["Run File System & Data Recovery Modules"]
    E --> F[Locate Deleted Files in Results]
    F --> G[Recover and Export Deleted Files]
```
## DESIGN STEPS:
### Step 1:
Open Autopsy and create a new case with appropriate case details.

### Step 2:
Add a disk image as a data source and let Autopsy analyze the content.

### Step 3:
Navigate to the "Deleted Files" section in Autopsy and examine or recover the deleted files.

## PROGRAM:
### Install Autopsy
```bash
# Download Autopsy from:
# https://www.autopsy.com/
# Install following the setup wizard.
```
### Create a New Case
```
# File → New Case
# Enter Case Name: Deleted_File_Recovery
# Choose Base Directory: C:\Cases\Deleted_File_Recovery
# Click Finish
```
### Add Disk Image
```
# Add Data Source → Disk Image or VM File
# Browse to: C:\forensics\disk.dd
# Click Next
```
### Run Ingest Modules
```# Select:
# - File System Analysis
# - Keyword Search (optional)
# - Data Recovery / Carving
# Click Finish
```
### Locate Deleted Files
```
# Navigate to 'Deleted Files' section in the tree view
# Review metadata (size, hash, timestamps)
```
### Export Deleted Files
```
# Right-click → Extract File(s)
# Save to: C:\forensics\Recovered_Files\
```

## OUTPUT:
Recovered Deleted File List and Details
<img width="1703" height="890" alt="image" src="https://github.com/user-attachments/assets/62396ee1-0af1-4145-911a-e4c36da13784" />
<img width="976" height="576" alt="image" src="https://github.com/user-attachments/assets/1eece84d-b5ee-4283-82c7-afc1955086d8" />
<img width="1078" height="677" alt="image" src="https://github.com/user-attachments/assets/b1e9bb2e-8f2c-4f95-b6c7-37c5135ba640" />
<img width="1072" height="673" alt="image" src="https://github.com/user-attachments/assets/d3a3a871-c474-4809-86a3-dc5e265489c1" />
<img width="1077" height="666" alt="image" src="https://github.com/user-attachments/assets/83e45126-7f8d-4958-bc6c-12cc79fd1190" />
<img width="1915" height="745" alt="image" src="https://github.com/user-attachments/assets/52cf1d8e-2d19-452c-ab68-141c3ecc96a9" />
<img width="1610" height="994" alt="image" src="https://github.com/user-attachments/assets/da7a5ad3-9359-4f71-ae23-60dd51581e1b" />
<img width="1621" height="926" alt="image" src="https://github.com/user-attachments/assets/360da0d4-9544-427d-956a-e7c228c10280" />
<img width="1901" height="1012" alt="image" src="https://github.com/user-attachments/assets/2f86f353-afec-4ab2-a3e1-5b96c41e7392" />
<img width="1666" height="983" alt="image" src="https://github.com/user-attachments/assets/5a2baaad-d550-4499-9ba9-5f2e71c07543" />


## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
