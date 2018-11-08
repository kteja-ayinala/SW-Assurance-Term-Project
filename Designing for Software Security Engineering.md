
# Designing for Software Security Engineering
**CSCI - 8420:  Assurance Army**

Aaron Kirby, Krishna Teja Ayinala, Sindhura Bonthu   </br>

Project: Nuxeo

# Threat model developed using Microsoft TMT for the Nuxeo project 
[Thraet Model Files](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/tree/master/Threat%20Model%20files/Final%20Threat%20Model) </br>
[Thraet Model Report](http://htmlpreview.github.io/?https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Threat%20Model%20files/Final%20Threat%20Model/Threat%20Model%20Assurance%20Army.html)

# Summary of Design related issues in the Nuxeo project

Nuxeo has successfully mitigated major threats across the important data flows. Nuxeo has provided strong authentication mechanisms which prevents unauthorized access to the sensitive information. It has implemented authentication techniques such as two-factor authentication and other authentication protocols. More details about authentication can be found at - [nuxeo authentication](https://doc.nuxeo.com/nxdoc/authentication-and-user-management/) </br>

Nuxeo mitigates data flow interruptions by using HTTP and HTTPS Reverse-Proxy Configuration. More details about implementations can be found at- [http/https reverse proxy configuration](https://doc.nuxeo.com/nxdoc/http-and-https-reverse-proxy-configuration/) </br>

Nuxeo protects the data in the application and during transfer using standard encryption techniques that prevent unnecessary information disclosure. More details about encryption can be found at - [nuxeo encryption]( https://doc.nuxeo.com/nxdoc/sensitive-configuration-data-encryption/) </br>

Nuxeo has version control repository which keeps track of all the data modifications. It allows users to easily revert to a specific version of document just by clicking on the version number. Nuxeo’s version control repository creates immutable, archived version of the document. More details about versioning can be found at - [nuxeo versioning](https://doc.nuxeo.com/nxdoc/versioning/#concepts) </br>

Nuxeo allows remote monitoring of server through Secure Shell. More details about SSH can be found at - [SSH remote access](https://doc.nuxeo.com/nxdoc/remote-monitoring-through-a-ssh-tunnel/) </br>

Nuxeo allows user to implement time-out when the application is not in use for a specific time period. It also provides security recommendations to the config files such as avoid sending server version, ability to prevent cross-side scripting, accepting only SSL high quality ciphers. More details about security recommendations can be found at - [nuxeo security recommendations](https://doc.nuxeo.com/nxdoc/security-recommendations/)




**Github Project Board:** https://github.com/kteja-ayinala/SW-Assurance-Term-Project/projects/4
