# Requirements for Software Security Engineering
**CSCI - 8420:  Assurance Army**

Aaron Kirby, Krishna Teja Ayinala, Sindhura Bonthu     

# Data flows: (Admin, Users, Database, Drive, VCS)

1) Form and set group permissions. (Authentication)
2) Edit,save,modify data to the cloud. (Encryption) 
3) Store and retrieve data from the db, drive. (Third-party)
4) Export data into different formats, specific permissions on RWX.(read, write, download)
5) Maintaining proper VCS of modifications on the shared doc. ( Audit )

# Security related configuration and installation issues

Nuxeo has an [issue tracking website](https://jira.nuxeo.com/browse/NXP/?selectedTab=com.atlassian.jira.jira-projects-plugin:issues-panel) that conveniently breaks down issues and categorizes them according to priority, components involved, and issue status. The website includes a search function that allows you to filter for specific parameters as well.

The most obvious components with security related issues are [Authentication](https://jira.nuxeo.com/browse/NXP-24580?jql=project%20%3D%20NXP%20AND%20resolution%20%3D%20Unresolved%20AND%20component%20%3D%20Authentication%20ORDER%20BY%20priority%20DESC), [Security](https://jira.nuxeo.com/browse/NXP-24539?jql=project%20%3D%20NXP%20AND%20resolution%20%3D%20Unresolved%20AND%20component%20%3D%20Security%20ORDER%20BY%20priority%20DESC), and [Security/Rights](https://jira.nuxeo.com/browse/NXP-19431?jql=project%20%3D%20NXP%20AND%20resolution%20%3D%20Unresolved%20AND%20component%20%3D%20%22Security%20%2F%20Rights%22%20ORDER%20BY%20priority%20DESC). However, among all 3 component categories, most of the current unresolved issues relate to authentication and permissions. Login issues are common, but most have already been resolved. Some of the current issues include setting ownership of private packages, group user permissions, and errors changing user permissions. Though, most of the issues are improvements to current features or known bugs. Some of the more substantial issues involve error handling stopping stream processing, document synchronization not keeping any records of the documents downloaded, and validation of third party databases.

