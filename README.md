# FileManager

An Excel Based File Management utility for Windows Operating System

## Features

1. Recursive **Tracing** of all files within a given folder and its sub folders
2. Recursive **Extraction** of all the zip files (including nested zip files) within a given folder and its sub folders
3. **Matches** file descriptions to the traced files when a file description index is provided
4. **Copy** filtered subset of traced files (with / without the folder structure + optional rename functionality)
5. Bulk **convert** Office files to PDF / HTML formats
6. **Duplicate detection** and Change tracking based on File hashes

## Pre-requisites

A one-time setup of pre-requisites must be done in-order to use this utility.

1. Open the windows **Command Prompt** (Start -> cmd)
2. Copy and Paste the below mentioned **one time setup script** into the command prompt and **hit Enter key**
3. Accept the terms for du.exe (Disk Usage)

### One time Setup script

```cmd
powershell -command Invoke-WebRequest https://github.com/engineered-in/FileManager/releases/latest/download/Utils.zip -OutFile "%temp%\Utils.zip"
powershell -command Expand-Archive "%temp%\Utils.zip" -DestinationPath "%localappdata%" -Force
%localappdata%/Utils/du.exe %temp% > %temp%/du.txt
echo "FileManager > Prerequisite Setup Successful! > ☺" & timeout 5 > NUL & exit
echo "."
```

### What will be downloaded during the One time Setup?

| Id. | Prerequisite | Description                            | Publisher  | About the Prerequisite              |
| --- | ------------ | -------------------------------------- | ---------- | ---------------------------------- |
| 1.  | [du.exe](https://docs.microsoft.com/en-us/sysinternals/downloads/du)       | Disk Usage                             | Microsoft  | Used to compute folder size        |
| 2.  | [fciv.exe](https://docs.microsoft.com/en-us/troubleshoot/windows-server/windows-security/fciv-availability-and-description)     | File Checksum Integrity Verifier       | Microsoft  | Used to generate SHA512 File Digest (Hash) |
| 3.  | [7z.exe](https://www.7-zip.org/)       | 7-Zip                                  | Open Source| Used to extract zip files           |
| 4.  | [7z.dll](https://www.7-zip.org/)       | 7-Zip                                  | Open Source| Used to extract zip files           |
