#!/usr/bin/env groovy

pipeline {
    agent any {
        
     stages {
     // Check out the test cases from github
     stage('test cases check out')
     {
         echo 'checking out source code'
             git 'https://github.comcast.com/StreamingServices/VDE-Fitnesse'
     }
      //build the test cases using ant and generate a jar
      stage('build testcases')
     {
         echo 'building the source code using ant'
             git 'https://github.comcast.com/StreamingServices/VDE-Fitnesse'
     }
         
     // Transfer and execute the jar file
      
      stage('transfer and run')
         {
             echo 'transfer and execute the jar file'
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
     
    }
    }
