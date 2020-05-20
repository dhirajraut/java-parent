pipeline {
    agent any
    tools {
        maven 'apache-maven-3.5.0-OOTB'
        jdk 'JDK_14.0.1'
    }
    stages {
        stage ('Initialize') {
            steps {
                    bat "echo PATH = %PATH%"
                    bat "echo M2_HOME = %M2_HOME%"
            }
        }

        stage ('Build') {
            steps {
                bat "mvn clean install" 
            }
            post {
                success {
                }
            }
        }
    }
}