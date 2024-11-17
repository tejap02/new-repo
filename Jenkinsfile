pipeline {
    agent any
    
    tools{
        maven 'm2'
    }
    
    stages {
        stage('checking softwares') {
            steps {
                bat "mvn --version"
            }
        }
        stage('clone the repos') {
            steps {     
                echo "Welcome"
                // git branch: 'main', credentialsId: 'tejap02', url: 'https://github.com/tejap02/new-repo.git'
            }
        }
         stage('clean old build and create new build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('check java version') {
            steps {
                bat 'java -version'
            }
        }
    }
}