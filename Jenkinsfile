pipeline {
    agent {
        label "windows"
    }
    tools {
        maven 'Maven3.1.1'
        jdk 'java8'
    }
    stages 
    {
       stage("download")
          {
             git "https://github.com/snmsoodan/testLmsAdmin.git"

          }
      stage("build")
          {
              sh 'mvn clean package'
          }
      stage("archive")
           {
              archiveArtifacts 'target/*.jar'
           }
      
   }
    
}
