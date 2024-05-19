# Jenkins-continuous integration Pipeline 
<img src="https://cdn.hashnode.com/res/hashnode/image/upload/v1711369871971/7ca7a359-0c7b-42a0-b870-5f083bd2895c.jpeg?auto=compress,format&format=webp" alt="">

# Kindly Follow  the above file procedure and Create the Entite CI of Jeniks 

# A Overview Procedure 

JENKINS AND GIT
1. Login to AWS Account and Install the Jenkins in ec2 Launched 
2. Create Keypair in AWS
3. Create Security Group (Port 22) 
   - 8080  -  Jenkis
   - 808   -  Nexus
   - 80    -  SonarQube
  
4. Launch 3 Instance in EC2 - For ( Jenkins, Nexus, SonarQube) - with the UserData and Login to     3 instaces PUTTY tool (For:Windows)
5. Install Plugins for - Maven,Git,Nexus,SonarQube,Slack,BuildTimeStamp,JDK
6. HandShake of Git with Jenkins
   -- Create the key in SSH - in jenkin Instance and store it in GIT SSH
   -- Create the WebHooks in GIT and give it in Jenkins in order to trigger git
7.  Build the Pipeline in jenkins - with GIT as the Source and Credentials
  
JENKIN - SONARQUBE
1. To handShake the SonarQube and Jenkin - In the SonarQube Server generate the token in sonarqube and give it in Jenkin
2. To handShake the SonarQube and Jenkin - In the jenkin generate the webhooks and give it in sonarqube - Now sonar able to receive the responses from jenkins

JENKIN SLACK
For Notification - We use Slack - For usage Genarate the token in slack and give it in jenkins'

# Now SonarQube, Jenkins,slack - are connected 

AWS
1. create the IAM Role
   -- EC2 Container Register FullAccess
   -- ECS Full Access
2. Create the ECR - In Private - copy the URL
3. Now give the Credentials of IAM in Jenkins
4. In ECS - Create the Cluster and Task Definition 
