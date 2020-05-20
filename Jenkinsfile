pipeline {
    agent any
    tools {
        maven 'apache-maven-3.5.0-OOTB'
        jdk 'JDK_14.0.1'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''

                '''
            }
        }

        stage ('Build') {
            steps {
                sh 'mvn clean install' 
            }
            post {
                success {
                    junit 'target/surefire-reports/**/*.xml' 
                }
            }
        }
    }
}