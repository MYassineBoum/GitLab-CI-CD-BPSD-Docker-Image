![image](https://github.com/MYassineBoum/GitLab-CI-BPS-Docker-Image/assets/115194839/efc66a4f-07d8-439c-bee1-f8df9ccb2a6f)# GitLab-CI-BPS-Docker-Image
To use the image of my Spring Boot CRUD application, you can simply type the following command:
<br/><br/>
<code>docker pull myassineboum/gitlab-ci-pipeline:v1</code>
<br/><br/>
I've added container_scanning, it's a good practice because it helps reducing vulnerabilities and risks by analyzing container images.
<br/>
For caching, it's a way to speed up the CI process.
<br/><br/>
Adding the following lines of code, we get the Vulnerability Report:
<code>
<br/>
variables
<br/>
    MAVEN_OPTS: "-Dmaven.repo.local=.m2/repository"
<br/><br/>
include:
<br/>
  - template: Security/SAST.gitlab-ci.yml
<br/><br/>
stages:
<br/>
    - install
    - build
    - test
    - scan
<br/><br/>
sast:
<br/>
  stage: test
</code>
<br/>
![image](https://github.com/MYassineBoum/GitLab-CI-BPS-Docker-Image/assets/115194839/ce88f5cc-beda-4819-982d-da41985c4895)
