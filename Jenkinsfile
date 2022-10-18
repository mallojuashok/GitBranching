pipeline {
    agent any
     triggers {
        pollSCM('0 5 * * *')
     }
    stages{
        stage('VCS'){
            steps{
                git branch:'feature', url:'https://github.com/mallojuashok/MyPracticeRepo.git'
            }
        }
        stage('Merge'){
            steps{
                sh git checkout release
				sh git merge feature --no-ff
            }
        }
        
        }
 }