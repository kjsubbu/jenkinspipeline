Deliverables: This demonstration will simulate a completely automated CI/CD deployment pipeline using Jenkins. It will essentially do the following steps (phases):

Pull the source code for a Java EE based Project from GIT. (SCM AUTOMATION)
Compile (build) the code using Maven to generate the .war file (BUILD AUTOMATION)
Run Test cases & ensure they pass. (TEST AUTOMATION)
Copy the .war to a Docker build workspace (DEPLOYMENT AUTOMATION)
Build a Docker image for Jboss server to run the war file. (DEPLOYMENT AUTOMATION)
Deploy the Docker container on a target node. (DEPLOYMENT AUTOMATION)
Prerequisites: This demonstration has the following prerequisites:

Jenkins should be installed with git, maven and shell plugins.
In Jenkins Server install using # yum -y install git maven docker before trying out this demo.
Changes to be made for Jenkins to be able to run docker.
echo "jenkins ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
echo 'Defaults:jenkins !requiretty' >> /etc/sudoers
setenforce 0 # Else disable SELINUX in /etc/sysconfig/selinux  and reboot
Execution: Add a Jenkins Build Job As per the below screenshot and build it:

Note: Add the build commands from the jenkins_build_commands.md file.
Jenkins build job Jenkins build job Jenkins build job Jenkins build job Jenkins build job
