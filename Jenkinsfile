pipeline {
    agent any {
     stages {
     
     stage('test cases check out')
     {
         echo 'checking out source code'
             git 'https://github.comcast.com/StreamingServices/VDE-Fitnesse'
     }
      stage('build')
     {
         echo 'building the source code using ant'
             git 'https://github.comcast.com/StreamingServices/VDE-Fitnesse'
     }
     
     }
     
    }
    }
