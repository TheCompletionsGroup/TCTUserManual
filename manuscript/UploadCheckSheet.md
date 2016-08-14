{#UploadCheckSheet}
{#UploadPreservation}
{#UploadProgressDocument}
#Upload or Complete a Barcoded Check Sheet, Preservation, or Other Progress Document

When check sheets, preservations, or other progress-related documents have been signed off, they can be saved to the project, thus officially "completing" a task (such as a check sheet). Uploading these documents contributes to the progress of the project.

The uploaded document may contain multiple check sheets so long as each sheet starts with a barcode. Pages following a barcoded sheet are considered attachments for that sheet and will be included when the document is split during the upload process. 
 
1. To complete a check sheet, preservation or other progress document, from the Menu, click **Menu > Progress > Upload**.   
![Menu > Progress > Upload](images\MPRogressUpload.PNG)   

1. Select files by dragging and dropping them from a Windows folder into the **Drop files here** box on the right, or click the **Browse** button to navigate to the file.    
![Upload Progress Documents](images\UploadProgressDocs.png)  

The **Upload Date** defaults to today's date, but if necessary, you can choose another date.  

1. Click **Upload**. A scanning progress page shows the progress of the processing of the files.  
![File Processing Progress](images\UploadcheckSheetScanProgress.png)

#Uploading a Check Sheet Without a Barcode

If there are check sheets which do not have a barcode because they were not generated from The Completions Tool they may be manually loaded. 

1. Click **Menu > Progress > Manual Check Sheet Upload**.   

![Manual Check Sheet Upload](images\ManualCheckSheetUpload.jpg)

1. Select the tag, check sheet and completion date. 

![Manual Check Sheet Upload](images\ManualCheckSheetUpload2.jpg)

1. Click **Choose File** and select the document to upload. 

1. Click **Upload**

#Uploading a Batch of Check Sheets Without Barcode

If the project is making use of the **Status Upload** functionality then documents must be uploaded separtely from the completion status. This can be done in bulk by directly adding the files to an Azure bucket and then requesting processing. Most projects will not use this functionality so check with your administrator before embarking on it. 

1. Upload the Work Assignment Progress CSV status document. The check sheets must show as complete in the system before documents are added to them. 

2. Open the tool your administrator recommended for connecting to Azure. [Azure Storage Explorer](http://storageexplorer.com/) is an excelent tool for this purpose and is available free of charge. It allows adding files directly to a staging area which is used to hold documents before they are processed and added to the system. 

3. Open the storage explorer and select **Connect using your Storage Account Information**

![images/storageExplorer1.jpg](images\storageExplorer1.jpg)

4. Enter the storage account name given to you by your administrator. 

5. Select **Use an account and a key to connect to an Azure Storage Account**. 

![images/storageExplorer2.jpg](images\storageExplorer2.jpg)

6. Enter the account name and key given to you by your administrator. The key is very complicated so using cut and paste is highly advisable. 

![images/storageExplorer3.jpg](images\storageExplorer3.jpg)

7. Click **Connect**

8. You will now be connected to the Azure Storage Account. Under **Blob Containers** on the left hand panel you will find a series of folders named after the Ids of the projects used in The Completions Tool. Depending on your set up you may have one or many. Consult with your administrator for a mapping of Id to project name. 

9. Drag files to the folder for your project. **Note:** Files must be named <Tag Number>_<Check Sheet Number>.pdf. Thus the E-008B check sheet for the tag AL-9993-03 would be named `AL-9993-03_E-008B.pdf`.

10. In The Completions Tool click **Menu > Imported Documents**. 

11. Click **Progress Documents**. Documents will be processed by the system. They are processed in batches of 250 documents so if you've uploaded more than 250 documents you may need to run multiple passes. Any problems will be reported on the page for manual resolution. Typically the problems are that the document has been named incorrectly or the work assignment has yet to be completed via the **Status Upload**.  