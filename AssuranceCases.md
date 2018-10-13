# Assurance Cases

Assurance Army

1. The Nuxeo Platform's login authentication protocols minimize unwanted access
![Case 1:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Assurance%20case%20diagrams/Assurance%20Cases%20-%20AA%20-%20Claim1.png)

[1] https://doc.nuxeo.com/nxdoc/authentication-and-user-management/ Default Authentication Mode - Login Page<br>
- The same section contains information about both password acceptance and password change<br>

[2] https://doc.nuxeo.com/nxdoc/nuxeo-duoweb-two-factor-authentication/<br>
- This addon is an outside application that is integrated into Nuxeo's security measures. Evidence to it's security capabilities would require delving into it's system.<br>

[3] https://doc.nuxeo.com/nxdoc/using-oauth2/#authorization-endpoint<br>
- Details the procedures for 3rd party access
-----------------------------------------------------------------------------------------------------------------------------
2. The Nuxeo platform prevents unauthorized access to sensitive data
![Case 2:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Assurance%20case%20diagrams/Assurance%20Cases%20-%20AA%20-%20Claim2.png)


[1] https://doc.nuxeo.com/nxdoc/sensitive-configuration-data-encryption/#page-title Using different ciphering algorithms.<br>
- Nuxeo uses advanced encryption algorithms such as AES/DES.<br>
[2] https://doc.nuxeo.com/nxdoc/sensitive-configuration-data-encryption/#encrypting-with-key-from-keystore Encrypting with Key from KeyStore - Decrypt with a key from a keystore<br>
- Details the procedure to encode the encryption key.<br>
-----------------------------------------------------------------------------------------------------------------------------
3. The Nuxeo Platform access permissions prevent unwanted modification to files
![Case 3:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Assurance%20case%20diagrams/Assurance%20Cases%20-%20AA%20-%20Claim3.png)

-----------------------------------------------------------------------------------------------------------------------------
4.  Nuxeo version control mitigates undesired effects from altered documents
![Case 4:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Assurance%20case%20diagrams/Assurance%20Cases%20-%20AA%20-%20Claim4.png)

[1]https://doc.nuxeo.com/nxdoc/versioning/ Automatic Versioning<br>
- There are different rules for altering your own documents or another user's<br>

[2]https://doc.nuxeo.com/nxdoc/security-policy-service/ Document Security Checks<br>
- Even if access to the system is gained, documents require permissions to view, edit, and delete

[3]https://doc.nuxeo.com/nxdoc/vcs/#easy-and-safe-hot-backup Easy and Safe Hot Backup
- Sort of a double backup to prevent document loss
----------------------------------------------------------------------------------------------------------------------------------------
5. Data transfers in Nuxeo are secure
![Case 5:](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Assurance%20case%20diagrams/Assurance%20Cases%20-%20AA%20-%20Claim5.png)

-----------------------------------------------------------------------------------------------------------------------------
Github Project Board: https://github.com/kteja-ayinala/SW-Assurance-Term-Project/projects/3
