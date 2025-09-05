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

STEP 1 :  CREATING A NEW DISK  (DISK 1)
•	Go to the start menu of your desktop and open Disk Management. Create a partition of your already available Local Drive. 
                  
 <img width="618" height="565" alt="image" src="https://github.com/user-attachments/assets/2ee1a21d-2670-4638-b61b-73e82eb599e9" />

•	For creating a new disk, create a new unallocated space in the already available Disk 0. And then assign a drive letter to it and create a drive G: as shown. This drive has 2 GB capacity.

<img width="944" height="91" alt="image" src="https://github.com/user-attachments/assets/506df229-2ae4-4239-adfb-495789b09bfa" />

•	Now go to Action tab and choose Create VHD

<img width="298" height="330" alt="image" src="https://github.com/user-attachments/assets/7347c025-aad9-49b6-a546-82e3037cac43" />

•	Now choose the location where you want to store your VHD and assign it a name. Then choose the other specifications as shown and click OK.

<img width="944" height="169" alt="image" src="https://github.com/user-attachments/assets/ece05ef8-2a60-4c0e-886a-6a01959d4591" />

•	Now the new Disk (Disk 1) is created. Now right click on the unallocated space in Disk 1.

<img width="434" height="541" alt="image" src="https://github.com/user-attachments/assets/a040325e-ad0a-4206-8936-06ef5f80dc1f" />

• Choose New Simple Volume

<img width="410" height="346" alt="image" src="https://github.com/user-attachments/assets/4abfbaaf-e6e6-4d61-a39a-870f6a22b0b2" />

•	A wizard opens

<img width="665" height="519" alt="image" src="https://github.com/user-attachments/assets/3b1cd4e5-f536-4176-af61-54850d1d9046" />

<img width="588" height="464" alt="image" src="https://github.com/user-attachments/assets/62532015-5f09-4b04-aff2-fe8e2ed0d65d" />

•	Click next -> Then in this page choose any letter for your drive.

<img width="380" height="300" alt="image" src="https://github.com/user-attachments/assets/e36072b4-f388-4306-bff1-4d4a4a6b4bf5" />

•	Click Next then Finish

<img width="669" height="193" alt="image" src="https://github.com/user-attachments/assets/ed92bbc4-0775-4100-8c73-6b1b98d9ffd3" />

STEP 2:  ADDING FILES INSIDE THE NEWLY CREATED DRIVE

•	In your PC you can view the new drive created

<img width="555" height="433" alt="image" src="https://github.com/user-attachments/assets/9fac7dbf-71d9-4e8c-bb69-49878a88ffa1" />

<img width="944" height="181" alt="image" src="https://github.com/user-
attachments/assets/f0fe175f-47c3-47c8-96af-1c52ee7f3b93" />

•	Inside it, add some image files as shown.

<img width="487" height="310" alt="image" src="https://github.com/user-attachments/assets/ebb81956-f40c-40d9-aaf5-6ac971dc8e17" />

•	Then, delete some files 

<img width="867" height="393" alt="image" src="https://github.com/user-attachments/assets/4e0d1d91-3362-49a8-a3d3-26a1510260f2" />

STEP 3: CREATING A DISK IMAGE USING FTK IMAGER

•	Open FTK Imager and go to File tab and choose Create Disk Image

<img width="455" height="385" alt="image" src="https://github.com/user-attachments/assets/8037fe50-464f-4158-a5df-553abb0271ed" />

•	Select the Source type as Physical Drive

<img width="585" height="483" alt="image" src="https://github.com/user-attachments/assets/06495004-e5ca-4f62-9bdc-a62c7186e7c4" />

•	Choose the Virtual Disk (Disk 1)

<img width="645" height="527" alt="image" src="https://github.com/user-attachments/assets/3696c3a7-bb38-436a-b924-1ea490bef34a" />

•	Choose the Add option

<img width="412" height="371" alt="image" src="https://github.com/user-attachments/assets/a97eedd4-b405-4583-9682-4dccf8547cb6" />

•	Choose the image type as .E01

<img width="443" height="324" alt="image" src="https://github.com/user-attachments/assets/a5ca41e9-1180-4db5-993f-b381f1124790" />

•	Choose the image destination and give start.

<img width="672" height="488" alt="image" src="https://github.com/user-attachments/assets/1479ed13-5969-4bd5-8dd8-cfd100495377" />

<img width="673" height="475" alt="image" src="https://github.com/user-attachments/assets/a586afe0-5d30-4928-9f4e-2b86bdc06316" />


STEP 4: VIEW THE DELETED FILES USING AUTOPSY TOOL

•	Go to your start menu and open Autopsy as an Administrator.

<img width="395" height="347" alt="image" src="https://github.com/user-attachments/assets/739828ec-ae95-4c1a-ad36-a3322ac3e52c" />

•	Select the New Case option when the dialog box opens.

<img width="449" height="306" alt="image" src="https://github.com/user-attachments/assets/bd6602b1-3f5f-4485-9cb7-d4c220717b62" />

•	Type the necessary details as shown. In the base directory choose the directory where you want to store the details of this case and where you want the recovered data to be stored. Preferably, choose the same drive from where you deleted the files. Then click on Next.

<img width="518" height="314" alt="image" src="https://github.com/user-attachments/assets/c9b20b99-8819-4896-b9f4-ae007c06a36f" />

•	Fill in necessary details and click Finish.

<img width="492" height="299" alt="image" src="https://github.com/user-attachments/assets/0c3910aa-2b5a-4ae1-94c1-91015f7e4510" />

•	The Case will be created. Such a window will be visible.

<img width="769" height="393" alt="image" src="https://github.com/user-attachments/assets/9803e12a-ddea-43bc-8a39-a6738ce97c88" />

•	Now that the case has been created choose the Add Data Source option under the File tab. Select the Host as shown and click Next.

<img width="802" height="509" alt="image" src="https://github.com/user-attachments/assets/8568533b-15b1-4dd3-8008-45797fcf9bae" />

•	Under Select  Data  Source Type, choose Disk Image or VM File and click Next

<img width="776" height="486" alt="image" src="https://github.com/user-attachments/assets/efc915ad-5b84-4c09-b2be-a3968bc86716" />

•	Now under Select Data Source choose the disk image from which data has to be recovered.

<img width="838" height="537" alt="image" src="https://github.com/user-attachments/assets/17e7fdc2-ba19-46b8-83dd-b6744148bf5a" />

•	Click Finish and then the following screen will be displayed. In this screen to see whatever was deleted from this drive, click the Deleted  Files option from the left pane as shown.

<img width="797" height="424" alt="image" src="https://github.com/user-attachments/assets/15bbeb96-fe4e-47e2-b58c-5c79d6a69498" />

•	On clicking the Deleted Files option, such a screen will be visible

<img width="520" height="271" alt="image" src="https://github.com/user-
attachments/assets/8bc2922e-286d-49a0-b37b-04020f3a1b44" />

STEP 5:   RECOVERING THE DELETED FILES

•	Select the files that you want to recover and right – click on them. Select the Extract File (s) option.

<img width="573" height="532" alt="image" src="https://github.com/user-attachments/assets/dee8b0a9-8315-4efc-ac1f-b12353438fa0" />

•	Now to view the recovered files, go to that drive and click on the Case folder created inside this drive.

<img width="788" height="506" alt="image" src="https://github.com/user-attachments/assets/2aa5acfd-8130-445e-8ca8-3670b6fb1d8d" />

•	Inside that folder, go to the Export Folder.

<img width="591" height="557" alt="image" src="https://github.com/user-attachments/assets/4189d19d-79c6-4265-90d3-661c5b0aafcd" />

•	Inside that folder you can find your recovered files
<img width="858" height="446" alt="image" src="https://github.com/user-attachments/assets/99ed66d0-a325-4e9c-94fc-9a13214d8b35" />

## RESULT:
Deleted files were successfully retrieved and analyzed using Autopsy.
