# CloudTier-Storage-Tiering-SDK
The CloudTier Storage Tiering SDK is a [Hierarchical Storage Management (HSM)](https://www.easefilter.com/cloud/Hierarchical-storage-management.htm) file system filter driver development kit. It is a data storage technique that automatically moves data between high-cost and low-cost storage media. It allows you to free up on-premise storage capacity transparently,by moving out cooler data to the cloud storage, thereby reducing capital and operational expenditures.

The CloudTier Storage Tiering SDK provides you a simple and low-cost solution to integrate your on-premise storage to cloud storage infrastructure in a seamless, secure, and transparent fashion. There is no interruption to migrate your on-premise files to the remote cloud storage, so you don't need to change your existing applications and infrastructure. It uses the on-premises storage as a tier 0 storage (hot storage), uses the public cloud storage as a tier 1 storage (clod storage). So you can connect the cloud storage as a second tier. Your application can use the cloud storage just like the local storage without any changes.

![loudTier Storage Tiering Solution](https://www.easefilter.com/images/CloudTier.png)

## How Does The Storage Tiering Work
The storage tiering is a comprehensive technology to access the remote storage transparently. The CloudTier storage SDK integrates with the local file system. When an application accesses a stub file, the CloudTier Filter Driver will bring back the remote storage’s data back to the application or rehydrate the stub file as a normal physical file based on the recall policy.

A stub file looks and acts like a regular file, it has the same file attributes with the original physical file (file size, creation time, last write time, last access time), it also keeps the original file’s security. A stub file is a file with sparse file and reparse point attributes, your customized tag data can be embedded to the stub file. A stub file doesn’t take the storage space for the file data, it only keeps the meta data of the file.

![loudTier Storage Tiering Solution](https://www.easefilter.com/images/stub.png)

## The Use Cases of CloudTier Storage Tiering
Cloud storage tiering can be widely used in telecommunications, government, oil, medical and other industries.

1. **Healthcare Data Archiving.** Healthcare providers are increasingly required to retain patient medical record data for multi-year periods. Storage requirements for patient data can quickly escalate when the records include high resolution images and ultrasound content.
2. **Business Policy Mandated Data Archiving.** Companies can generate PB’s of data in the course of day to day operations and to meet legal compliance requirements. Archive Storage can work with Smart Archiving offerings from ISV’s to create a low cost, content archiving solution.
3. **Digital Media Content Retention.** Creators can generate PB’s worth of video and picture content that is used in the development of original digital media. Archive Storage gives creators a low-cost storage repository for original source content. File-level tiering makes it easy to shift from cold to hot storage should the need arise to use that content for another project.
4. **Security/Public Safety data retention.** As the number and sophistication of threats to personal and business safety continue to increase, so does the demand for video surveillance. Public and now private sector companies generate TB’s of surveillance footage daily in the course of protecting their citizens and assets. Archive Storage is a low-cost option for storing that data.

## [The CloudTier Storage Tiering Demo](https://www.easefilter.com/cloud/cloudtier-storage-tiering-demo.htm)
The CloudTier Storage Tiering Demo demonstrates how to use the SDK. After the stub file was generated, you can register the callback function for the file system filter driver. When the stub file was accessed, the callback function will be invoked, the callback function will retrieve the data from the remote server and send back to the filter driver.

1.	Create the stub files first, go to tools->create stub test files.
	By creating the stub file, you can move out your data to low-cost remote storage, 
        
2.	The test source folder stores the file data to simulate the remote host server. 
	You can store your source file data anywhere, i.e. Amazon s3, Azure storage or your own private cloud storage.

3.	The test stub file folder stores the test stub files.
	The stub file doesn't take the storage space, it only keeps the meta data you created.

4.	After the stub files were created, start the filter service. The stub files can be read as a regular file, when you open the stub file, 
	all data will read from the source file by the demo application.

5.	For demo purpose, the new stub file’s reparse point tag always pointing to the source file, you can change it to your remote sever, or in the cloud.


## EaseFilter File System Filter Driver SDK Reference
| Product Name | Description |
| --- | --- |
| [Storage Tiering SDK](https://www.easefilter.com/cloud/storage-tiering-sdk.htm) | EaseFilter Storage Tiering Filter Driver SDK Introduction. |
| [File Monitor SDK](https://www.easefilter.com/kb/file-monitor-filter-driver-sdk.htm) | EaseFilter File Monitor Filter Driver SDK Introduction. |
| [File Control SDK](https://www.easefilter.com/kb/file-control-file-security-sdk.htm) | EaseFilter File Control Filter Driver SDK Introduction. |
| [File Encryption SDK](https://www.easefilter.com/kb/transparent-file-encryption-filter-driver-sdk.htm) | EaseFilter Transparent File Encryption Filter Driver SDK Introduction. |
| [Registry Filter SDK](https://www.easefilter.com/kb/registry-filter-drive-sdk.htm) | EaseFilter Registry Filter Driver SDK Introduction. |
| [Process Filter SDK](https://www.easefilter.com/kb/process-filter-driver-sdk.htm) | EaseFilter Process Filter Driver SDK Introduction. |
| [EaseFilter SDK Programming](https://www.easefilter.com/kb/programming.htm) | EaseFilter Filter Driver SDK Programming. |

## EaseFilter SDK Sample Projects
| Sample Project | Description |
| --- | --- |
| [CloudTier Storage Tiering Demo](https://www.easefilter.com/cloud/cloudtier-storage-tiering-demo.htm) | A HSM File System Filter Driver Demo. |
| [Auto File DRM Encryption](https://www.easefilter.com/kb/auto-file-drm-encryption-tool.htm) | Auto file encryption with DRM data embedded. |
| [Transparent File Encrypt](https://www.easefilter.com/kb/AutoFileEncryption.htm) | Transparent on access file encryption. |
| [Secure File Sharing with DRM](https://www.easefilter.com/kb/DRM_Secure_File_Sharing.htm) | Secure encrypted file sharing with digital rights management. |
| [File Monitor Example](https://www.easefilter.com/kb/file-monitor-demo.htm) | Monitor file system I/O in real time, tracking file changes. |
| [File Protector Example](https://www.easefilter.com/kb/file-protector-demo.htm) | Prevent sensitive files from being accessed by unauthorized users or processes. |
| [FolderLocker Example](https://www.easefilter.com/kb/FolderLocker.htm) | Lock file automatically in a FolderLocker. |
| [Process Monitor](https://www.easefilter.com/kb/Process-Monitor.htm) | Monitor the process creation and termination, block unauthorized process running. |
| [Registry Monitor](https://www.easefilter.com/kb/RegMon.htm) | Monitor the Registry activities, block the modification of the Registry keys. |
| [Secure Sandbox Example](https://www.easefilter.com/kb/Secure-Sandbox.htm) |A secure sandbox example, block the processes accessing the files out of the box. |
| [FileSystemWatcher Example](https://www.easefilter.com/kb/FileSystemWatcher.htm) | File system watcher, logging the file I/O events. |

## Filter Driver Reference

* [Understand MiniFilter Driver](https://www.easefilter.com/kb/understand-minifilter.htm)
* [Understand File I/O](https://www.easefilter.com/kb/File_IO.htm)
* [Understand I/O Request Packets(IRPs)]https://www.easefilter.com/kb/understand-irps.htm)
* [Filter Driver Developer Guide](https://www.easefilter.com/kb/DeveloperGuide.htm)
* [MiniFilter Filter Driver Framework](https://www.easefilter.com/kb/minifilter-framework.htm)
* [Isolation Filter Driver](https://www.easefilter.com/kb/Isolation_Filter_Driver.htm)

## Support
If you have questions or need help, please contact support@easefilter.com 

[Home](https://www.easefilter.com/) | [Solution](https://www.easefilter.com/solutions.htm) | [Download](https://www.easefilter.com/download.htm) | [Demos](https://www.easefilter.com/online-fileio-test.aspx) | [Blog](https://blog.easefilter.com/) | [Programming](https://www.easefilter.com/kb/programming.htm)


