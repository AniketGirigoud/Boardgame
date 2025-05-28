pipeline {
    agent {label 'aniket'}
    
    tools {
        maven 'maven-2'
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
                    sh 'hello Jenkins Job is completed'                }
            }
        }
        
    }
    
