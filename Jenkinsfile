node('master') 
{
    stage('ContinuousDownload-Loans') 
    {
       git 'https://github.com/selenium-saikrishna/maven.git'

    }
    stage('ContinuousBuild-Loans') 
    {
      sh 'mvn package'
    }
    stage('ContinuousDeployment-Loans')
    {
        sh 'scp /home/vagrant/.jenkins/workspace/mul_test/webapp/target/webapp.war ubuntu@172.31.18.240:/var/lib/tomcat8/webapps/testenv.war'
    }
    stage('Continuoustesting-Loans')
    {
        git 'https://github.com/selenium-saikrishna/FunctionalTesting.git'
    }
    
    
 
    
    
    
}
