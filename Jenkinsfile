pipeline {
    agent any
    stages {
        stage("Maven Build") {
            when {
                branch 'dev'
            }
            steps {
            sh 'mvn clean package'
        }
        }
        stage("Sonar Analysis") {
            when {
                branch 'dev'
            }
            steps {
                echo "Sonar Analysis"
            }
        }
        stage("Dev Deploy") {
            when {
                branch 'dev'
            }
            steps {
                echo "Dev Deploy.."
            }
        }
         stage("Test Deploy") {
            when {
                branch 'test'
            }
            steps {
                echo "Test Deploy.."
            }
        }
         stage("Prod Deploy") {
            when {
                branch 'main'
            }
            steps {
                echo "Prod Deploy.."
            }
        }
    }
 
}

