pipeline {
    agent any
    tools {
        maven 'Maven 3.5.0'
        jdk 'jdk14'
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
					set M2_HOME = "C:\\Users\\draut\\00_Dhiraj\\Apps\\apache-maven-3.5.0-OOTB"
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
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