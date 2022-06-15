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

        stage ('Testing Stage') {

            steps {
                //withMaven(maven : 'maven_3_5_0') {
                    sh 'test'
                }
           // }
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