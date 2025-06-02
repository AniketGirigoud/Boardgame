pipeline {
    agent any
    
    tools {
        maven 'maven-1'
        jdk 'jdk17'
    }
    
    stages{
        stage('git checkout') {
            steps{
                git branch: 'main', url: 'https://github.com/jaiswaladi246/Boardgame.git'
            }
        }
        stage('validate') {
                steps{
                    sh 'mvn validate'
                }
            }
            stage('compile'){
                steps{
                    sh 'mvn compile'
                }
            }
            stage('test') {
                steps{
                    sh 'mvn test'
                }
            }
            stage('package') {
                steps{
                    sh 'mvn package'
                }
            }
            stage('install') {
                steps{
                    sh 'mvn install'
                }
            }
            stage("completed") {
                steps{
                    sh 'echo hello Jenkins Job is completed'                }
            }
        }
        
    }
    
