# Requirements for Software Security Engineering
**CSCI - 8420:  Assurance Army**

Aaron Kirby, Krishna Teja Ayinala, Sindhura Bonthu     

# Data flows: (Admin, Users, Database, Drive, VCS)

1) Form and set group permissions. (Authentication)
2) Edit,save,modify data to the cloud. (Encryption) 
3) Store and retrieve data from the db, drive. (Third-party)
4) Export data into different formats, specific permissions on RWX.(Read, write, download)
5) Maintaining proper VCS of modifications on the shared doc. (Audit)


# Security requirements for use cases using misuse case diagrams

1) System Admin wants to set user roles, while Poor Bank Clerk wants to steal money and transfer it to his Swiss bank account. His role permissions are not enough to accomplish the money transfer, so he needs to access admin permissions in order to change his user role. To accomplish this theft, Poor Bank Clerk uses a Brute Force Attack to guess the System Admin’s password. This attack is prevented by implementing a lock-out policy that locks the login system once too many incorrect passwords are attempted. Poor Bank Clerk will use a Signature Spoof and appear to have more authority than he actually possesses to gain access to bypass the lock-out policy. However, two-factor authentication will prevent the use of a Signature Spoof. <br>
![Case1:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Misuse%20case%20diagrams/case1.png)
2) Bank Manager wants to read and write data to the cloud, while DeadBeat Derrick wants to access this data to erase his debt amount. DeadBeat Derrick uses Buffer Manipulation to run his own commands and access the data. This attack is prevented by encrypting the data, but Deadbeat Derrick Drops the Encryption level to help his Buffer Manipulation succeed. SSL encryption is used to strengthen the encryption and prevent the attacks from succeeding.</br>
![Case2:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Misuse%20case%20diagrams/case2.png)
3) Bank Application Developer wants to modify some documents for a 3rd party application while the Competing Bank Hacker wants to ruin the application. He uses Content Spoofing to make changes to the application documents, but secure transfer protocols are implemented to mitigate this attack. Competing Bank Hacker then uses Data Interchange Protocol Manipulation to bypass transfer protocols, but then block-chain technology is used to strengthen the transfer protocols and prevent the attacks.</br>
![Case3:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Misuse%20case%20diagrams/case3.png)
4) Bank verification team wants to upload and download customer submitted customer documents, while Grad student with lots of free time wants to insert a virus into the bank system by sending an email with Infected Software. The email is acanned with anti-virus software prior to opening any attachments, but Grad student uses an Evercookie to save itself in the bank system and duplicate itself at a later time. An anti-cookie tool can be used to mitigate the Evercookie. </br>
![Case4:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Misuse%20case%20diagrams/case4.png)
5) The Banking System wants to track its version control modifications while the Disgruntled Bank Clerk wants to damage the bank data by altering or deleting it’s history. The VCS stores metadata to mitigate the effects of wrongly altered or deleted history. Disgruntled Bank Clerk tries to directly over-write the metadata, but his is prevented by making the metadate immutable. To help keep the bank data secure (which includes the above scenario) a System Admin will monitor a VCS using behavioral analytics to detect and unusual activity. </br>
![Case5:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Misuse%20case%20diagrams/case5.png)


# Alignment of Security requirements with advertised features

1)The nuxeo platform has the required authentication functionality where it allows the user to login with credentials and the complexity of the password can be check against a regular expression. Nuxeo also allows users to login with some other Authentication Protocols such as: SAML 2.0, OpenID, Two-factor authentication, Kerberos, CAS/CAS 2.0. The users of Nuxeo platform can also provide 'unauthenticated access' on some documents in order to make them accessible to anonymous users. The administrator can manage users' passwords.<br/>
More details about the nuxeo authentication are available at: </br> 
https://doc.nuxeo.com/nxdoc/authentication-and-user-management/

2)Data acccess is managed in the nuxeo platform. It provides various types of encryption such as: Binaries Encryption, FileSystem AES Encryption, S3 Encryption. More details about the nuxeo encryption is available at:</br>
https://doc.nuxeo.com/nxdoc/implementing-encryption/</br>
However, nuxeo doesnot provide SSL encryption.

3)

4)Security on content is available in the nuxeo platform, more details on data security is available at: 
https://doc.nuxeo.com/nxdoc/file-download-security-policies/

5)Nuxeo provides both manual and automatic versioning. Users with access rights can edit the document only after Checkout. An immutable, version of documents is created by Checkin operation. More details on versioning is available at:<\br> https://doc.nuxeo.com/nxdoc/versioning/

# Security related configuration and installation issues

Nuxeo has an [issue tracking website](https://jira.nuxeo.com/browse/NXP/?selectedTab=com.atlassian.jira.jira-projects-plugin:issues-panel) that conveniently breaks down issues and categorizes them according to priority, components involved, and issue status. The website includes a search function that allows you to filter for specific parameters as well. While there is not a section specific to installation issues, but there exists a [Configuration](https://jira.nuxeo.com/browse/NXP-17648?jql=project%20%3D%20NXP%20AND%20resolution%20%3D%20Unresolved%20AND%20component%20%3D%20Configuration%20ORDER%20BY%20priority%20DESC) component. Two of the more notable security related issues (that have since been resolved) include a faulty string [encryption](https://jira.nuxeo.com/browse/NXP-25257) not allowing an application to correctly start, and the Admin Center not being able to properly save database [elements](https://jira.nuxeo.com/browse/NXP-6816) such as name, user, password, host, and port. This issue tracker shows the evolution of Nexeo's various features.

Nuxeo provides a Core Developer Guide which goes through the [installation](https://doc.nuxeo.com/corg/) processes for the applications necessary to run Nuxeo. The only security related concern it addresses is when configuring the SSH key for data transfer with [GitHub](https://doc.nuxeo.com/corg/installing-git/). It doesn't discuss any issues with SSH, but simply says that it's required. This guide is to help open source developers get started quickly and easily.

For installing the actual Nuxeo system, [documentation](https://doc.nuxeo.com/) is provided on their website with section pertaining to [installation](https://doc.nuxeo.com/nxdoc/installation/). You can search for other security related documentation, and those of interest include:

[User authentication](https://doc.nuxeo.com/nxdoc/authentication-and-user-management/)

[Permissions](https://doc.nuxeo.com/nxdoc/security/)

[Repository Access Control List](https://doc.nuxeo.com/nxdoc/acls/)

[Permission checks for reading/writing](https://doc.nuxeo.com/nxdoc/nuxeo-security-system/)

[Additional custom security policies](https://doc.nuxeo.com/nxdoc/security-policy-service/)

[File download policies](https://doc.nuxeo.com/nxdoc/file-download-security-policies/)

This is just the tip of the iceberg as there exists extensive documentation that goes through the Nuxeo's security features. It is clear that Nuxeo has many layers of security involving user permissions and document access.

# GitHub project management

[Project](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/projects/2)

