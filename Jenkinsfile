pipeline {
    agent any

    stages {
        stage ('Compiling Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn compile'
                }
            }
        }
    stage('Test') {
        steps {
            sh 'Testing..'
                build 'Test'
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