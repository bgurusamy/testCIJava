#!/usr/bin/env groovy

pipeline {
    agent any 
        
     stages {
     // Check out the test cases from github
     stage('test cases check out')
     {
          steps{
         checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [[$class: 'CloneOption', depth: 0, noTags: false, reference: '', shallow: false, timeout: 25]], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '8fa4ce4a-7441-4cd3-85de-e137313adf1b', url: 'https://github.comcast.com/StreamingServices/VDE-Fitnesse.git']]])

        
      echo 'checking out source code'
          //git credentialsId: '8fa4ce4a-7441-4cd3-85de-e137313adf1b', url: 'https://github.comcast.com/NextVM/freeswitch.git'


         }
     }
         // build jar
         //start fitness
        // execute fitness
         //auto email 
         
      //build the test cases using ant and generate a jar
      stage('build testcases')
     {  steps
      {
         echo 'building the source code using ant'
             git 'https://github.comcast.com/StreamingServices/VDE-Fitnesse'
      }
      }
         
     // Transfer and execute the jar file
      
      stage('transfer and run')
         {
        steps
             {
             echo 'transfer and execute the jar file'
             }
         }
     }
         
       //Send the updates
         post
         {
             success{
                 echo 'success block'
             }
             failure
             {
                 echo 'failure block'
             }
         }
     
     
     
    }
    
