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

1) A Poor Bank Clerk should not be able to transfer money to his own account.
![Case1:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Misuse%20case%20diagrams/case1.png)
2) DeadBeat Derrick should not be able to erase his debt amount.
![Case2:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Misuse%20case%20diagrams/case2.png)
3) A Competing Bank Hacker should not be able to ruin the application.
![Case2:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Misuse%20case%20diagrams/case3.png)
4) Grad student with free time should not be able to insert virus into the Bank System.
![Case4:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Misuse%20case%20diagrams/case4.png)
5) Disgruntled Bank Clerk should not able to Alter/Detele history.
![Case5:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Misuse%20case%20diagrams/case5.png)


# Security requirements with advertised features

1)The nuxeo platform has the required authentication functionality, more details about the nuxeo authentication is available at: https://doc.nuxeo.com/nxdoc/authentication-and-user-management/
https://doc.nuxeo.com/nxdoc/nuxeo-duoweb-two-factor-authentication/

2)Data acccess is managed in the nuxeo platform, more details about the nuxeo authentication is available at:
https://doc.nuxeo.com/nxdoc/implementing-encryption/
https://doc.nuxeo.com/nxdoc/security/#managing-permissions-on-content


3)

4)Security on content is available in the nuxeo platform, more details on data security is available at: 
https://doc.nuxeo.com/nxdoc/file-download-security-policies/

5)Version control is maintained in the nuxeo platform which uses "immutable versioning". More details on versioning is available at: https://doc.nuxeo.com/nxdoc/versioning/

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

