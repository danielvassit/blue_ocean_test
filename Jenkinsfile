pipeline {

    agent any

    environment {
        FOO = "BAR"
    }

    stages {

        stage ('First') {

            tools {
                maven "mvn3.3.9"
            }

            steps {
                sh "echo 'This is first stage'"
            }

            post {
                always {
                    echo "post"
                }
            }
        }

        stage ('Second') {
            
            tools {
                maven "mvn3.3.3"
            }
            
            steps {
                sh "echo 'This is first stage'"
            }
        }

        stage ('Third') {
            steps {
                parallel(
                    one: {
                        echo "Parallel 1"
                    },
                    two: {
                        echo "Parallel 2"
                    },
                    three: {
                        echo "Parallel 3"
                    }
                )
            }
        }

    }

}