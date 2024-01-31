To use the image of my Spring Boot CRUD application, you can simply type the following command:
<br/><br/>
<code>docker pull myassineboum/gitlab-ci-pipeline:v1</code>
<br/><br/>
I've added container_scanning, it's a good practice because it helps reducing vulnerabilities and risks by analyzing container images.
<br/>
For caching, it's a way to speed up the CI process.
<br/><br/>
Enabling SAST on GitLab Ultimate, we get the Vulnerability Report:
<br/>
![image](https://github.com/MYassineBoum/GitLab-CI-BPS-Docker-Image/assets/115194839/ce88f5cc-beda-4819-982d-da41985c4895)
