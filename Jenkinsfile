#!/usr/bin/env groovy

pipeline {
    agent any 
        
     stages {
     // Check out the test cases from github
     stage('test cases check out')
     {
         steps{
         echo 'checking out source code'
             git (url:'https://github.comcast.com/StreamingServices/VDE-Fitnesse',
                  branch:'master',
                  credentialsId:'a7cb5dec-9051-40cb-942b-d8423f3be9bb'
             )
         }
     }
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
    
