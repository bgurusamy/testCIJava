#!/usr/bin/env groovy

pipeline {
    agent any 
        
     stages {
     // Check out the test cases from github
     stage('test cases check out')
     {
         steps{
         echo 'checking out source code'
           git credentialsId: '7af807f3-2f56-40a0-85a5-25a3dc909758', url:'https://github.comcast.com/StreamingServices/VDE-Fitnesse.git'

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
    
