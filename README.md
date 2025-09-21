# Reviewing-Unallocated-Space-Extracting-Data-with-Tools-Digital-Investigation-Processes
## AIM:
To review unallocated space in a disk image, extract data using forensic tools, and understand the digital investigation process.
## REQUIREMENTS
- Autopsy or FTK Imager
- Sleuth Kit (TSK)
- Hex Editor (e.g., HxD)
- Operating System: Windows 10/11 or Linux (Kali preferred)
## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Load into Autopsy or Sleuth Kit]
    B --> C[Identify Unallocated Space]
    C --> D[Scan for Data Signatures]
    D --> E[Carve and Recover Files]
    E --> F[Analyze Recovered Data]
    F --> G[Document Findings in Report]
```
## DESIGN STEPS:
### Step 1 (Acquire Evidence Image):
- Obtain the disk image in ```.dd``` or ```.E01``` format from a trusted forensic acquisition process.
- Verify hash values (MD5/SHA256) to maintain integrity.

### Step 2(Load Image into Forensic Tool):
- Open Autopsy or FTK Imager.
- Create a new case and add the evidence image.

### Step 3(Locate Unallocated Space):
- Navigate to the partition structure view.
- Identify sectors not assigned to any partition (unallocated).
### Step 4(Analyze & Carve Data):
- Use built-in data carving tools to search for file signatures (JPEG, DOCX, PDF, etc.).
- Preview carved files for relevance.
  
## PROGRAM:
| Step | Action                     | Tool Used                   | Output                       |
| ---- | -------------------------- | --------------------------- | ---------------------------- |
| 1    | Load disk image            | Autopsy / FTK Imager        | Partition & unallocated view |
| 2    | Identify unallocated space | Autopsy File System View    | Sector ranges                |
| 3    | Data carving               | Autopsy Data Carving Module | Recovered files              |
| 4    | Export evidence            | Autopsy Export Option       | File copies for analysis     |


## OUTPUT:
Unallocated Space Analysis and Extracted Data Report

<img width="1920" height="674" alt="Screenshot 2025-09-21 223222" src="https://github.com/user-attachments/assets/87bdbdbb-e5a3-4164-bef7-edf36f8e074c" />
<img width="1301" height="456" alt="Screenshot 2025-09-21 223520" src="https://github.com/user-attachments/assets/96b37ffc-e252-49dd-bb30-9e52647f52d7" />
<img width="1010" height="476" alt="Screenshot 2025-09-21 223325" src="https://github.com/user-attachments/assets/c51b716f-f3d1-4dd2-8536-30679939cbac" />
<img width="1918" height="1079" alt="Screenshot 2025-09-21 223622" src="https://github.com/user-attachments/assets/6db284c6-1aeb-4811-8fc1-9ec7ca08cc82" />
<img width="1920" height="1080" alt="Screenshot 2025-09-21 223703" src="https://github.com/user-attachments/assets/09139fb4-c524-403c-ad4b-1ccebd0d2fd5" />
<img width="1728" height="902" alt="Screenshot 2025-09-21 223905" src="https://github.com/user-attachments/assets/1fc7eb1b-0480-42a3-b461-bc3e1d3234ae" />
<img width="1704" height="926" alt="Screenshot 2025-09-21 223924" src="https://github.com/user-attachments/assets/1e6bdf52-6390-4be2-a5af-b04f4dd74787" />

## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.

