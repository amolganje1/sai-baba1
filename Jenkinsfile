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
   
}

