pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Mavena') {
                    bat "mvn clean install"
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'Mavena') {
                    bat "mvn test"
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'Mavena') {
                    bat "mvn deploy"
                }
            }
        }
    }
}