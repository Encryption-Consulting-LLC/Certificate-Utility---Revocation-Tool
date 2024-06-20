# Certificate Revocation Tool User Guide

## 1. INTRODUCTION

### 1.1 Purpose

This document provides a comprehensive user guide for the Certificate Revocation Tool. This application simplifies the process of revoking certificates listed in a CSV file. It offers a user-friendly interface to guide you through the steps, displays progress during revocation and deletion, and provides detailed logs for successful and failed attempts.

- This application will check for valid certificates provided from a .csv file. Operations will be performed only on valid active certificates.
- The script will prompt the user to confirm if they want to revoke/delete the certificates found form the .csv file.
- The script will also display the progress of the operations while they are underway, and maintain a detailed log for operations being performed.

### 1.2 Prerequisites

- CertUtil must be installed on the system where the application is being run.
- Ensure to take a snapshot or backup of the VM prior to running the application or performing defragmentation of the CA database.
- Domain Administrator account is required for using this application.
- Application must be executed on the Certification Authority.
- Active Directory domain services must be online.

### 1.3 System Requirements

- Windows Server 2019 or above
- .NET Framework v4.0.30319

## 2. USAGE

### 2.1 Launch the Application

Double-click the CertificateUtility_Revoke.exe file to launch the application. The application window will appear.

![Application Window](https://github.com/Encryption-Consulting-LLC/Certificate-Utility---Revocation-Tool/assets/159181390/693852f9-4e21-4ece-82f5-32544311dda9)

### 2.2 Select the CSV File

Click on ‘Browse’ button. The application will prompt you to select a CSV file containing certificate information. The expected format should have a necessary column "Serial Number".

### 2.3 Review Certificate List

Once you select the CSV file, the application will display details about the certificates provided for revocation.

![Review Certificates](https://github.com/Encryption-Consulting-LLC/Certificate-Utility---Revocation-Tool/assets/159181390/676d1643-4b35-49ec-afba-0bab95ac017d)

### 2.4 Proceed to Revocation

Click the "Next" button to proceed with the revocation process. The application will prompt you to confirm the operation.

### 2.5 Initiate Revocation

Click the "Start" button to initiate the revocation process for the listed certificates. The log box will display the status of each certificate revocation attempt. Messages will indicate success or failure for each certificate.

![Revocation Progress](https://github.com/Encryption-Consulting-LLC/Certificate-Utility---Revocation-Tool/assets/159181390/1aad193c-d6c0-4995-b167-8a41ca4b3910)


### 2.6 Exit Application

Click the "Finish" button to close the application after reviewing the revocation results.

### 2.7 Enable Certificate Deletion (Optional)

Select the checkbox labeled "Proceed to Delete after Revocation" (if available) to schedule the certificates for deletion after successful revocation.

![Delete Certificates Checkbox](https://github.com/Encryption-Consulting-LLC/Certificate-Utility---Revocation-Tool/assets/159181390/23c5e6ec-917f-4674-a73c-203fdcf83006)


### 2.8 Initiate Deletion (Optional)

Click the "Next" button to proceed with the deletion process after revocation is complete.

### 2.9 Start Certificate Deletion (Optional)

Click the "Start" button (if presented) to initiate the deletion of revoked certificates. The progress bar and log will update to reflect the deletion process. The log box will display the status of each certificate deletion attempt. Messages will indicate success or failure for each certificate deletion.

![Deletion Progress](https://github.com/Encryption-Consulting-LLC/Certificate-Utility---Revocation-Tool/assets/159181390/e4616e40-fa23-4238-970c-3b6a9e6061ff)


### 2.10 Exit Application

Click the "Finish" button to close the application after reviewing the deletion results.

## Additional Notes

- A log file containing detailed information about revocation and deletion (if applicable) will be saved to a designated location. (e.g., “C:\Users\Public\Documents\CertificateRevokeLogs\2024-06-19-12-53-57”)
- You can access the log folder by clicking the "Open Logs..." button
