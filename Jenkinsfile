pipeline {
    agent any

    stages {
        stage ('Git Checkout') {
            steps {
                git credentialsId:'https://github.com/thatboiilogic/bookstooread'

                }
        }

        stage ('Maven Build') {
            steps {
                    sh 'mvn clean package'
                }
            }



        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}