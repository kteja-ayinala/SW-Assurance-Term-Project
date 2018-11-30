# Code analysis for Software Security Engineering
**CSCI - 8420:  Assurance Army**

Aaron Kirby, Krishna Teja Ayinala, Sindhura Bonthu   </br>

Project: Nuxeo

# Code review Strategy
Nuxeo is a very large open-source project with copious amounts of code. We initially tried tools like SWAMP, findbugs and Sonarcloud to build and review the assesment reports. Because of the code base external dependencies [build requirements](https://github.com/nuxeo/nuxeo#building), we could not succed to build. So, we found a tool PMD which can review the code statically with out building it. We decided to review on PMD based on the JAVA rulesets. We also decided to manually review the parts of code which is related to our previous Assurance cases and Misuse cases which helped us to create an Checklist. We have followed Checklist based  and Scenario-based strategies.

# Findings from manual code review

# Findings from automated code scanning
[Full Report](https://github.com/kteja-ayinala/SW-Assurance-Term-Project/blob/master/Codereview%20reference%20links/Full-Report-nuxeo.xml)


**Github Project Board:** https://github.com/kteja-ayinala/SW-Assurance-Term-Project/projects/5
