node('master') 
{
   stage('ContinuousDownload') 
   {
     git 'https://github.com/selenium-saikrishna/maven.git'
   }
   stage('ContinuousBuild') 
   {
     sh label: '', script: 'mvn package'
   }
   stage('ContinuousDeployment')
   {
       sh label: '', script: ' scp /home/ubuntu/.jenkins/workspace/mul_master/webapp/target/webapp.war ubuntu@172.31.18.240:/var/lib/tomcat8/webapps/qaenv.war'
   }
   stage('ContinuousTesting')
   {
       git 'https://github.com/selenium-saikrishna/FunctionalTesting.git'
   }
   stage('ContinuousDelivery')
   {
       sh label: '', script: ' scp /home/ubuntu/.jenkins/workspace/mul_master/webapp/target/webapp.war ubuntu@172.31.37.128:/var/lib/tomcat8/webapps/masterprodenv.war'
   }
   
   
   
   
   
   
   
    
    
    
}
