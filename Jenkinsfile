node('master') 
{
   stage('ContinuousDownload') 
   {
      git 'https://github.com/intelliqittrainings/maven.git'
   }
   stage('ContinuousBuild')
   {
       sh 'mvn package'
   }
   stage('ContinuousDeployment')
   {
      sh 'scp /var/lib/jenkins/workspace/ScriptedPipeline_main/webapp/target/webapp.war ubuntu@172.31.33.13:/var/lib/tomcat9/webapps/qaapp.war'
   }
   stage('ContinuousTesting')
   {
       git 'https://github.com/intelliqittrainings/FunctionalTesting.git'
       sh 'java -jar /home/ubuntu/.jenkins/workspace/ScriptedPipeline_main/testing.jar'
   }
   
   
   
   
   
}

