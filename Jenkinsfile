pipeline {

    agent any

    stages {

        stage ('First') {

            tools {
                maven "mvn3.3.9"
            }

            steps {
                sh "echo 'This is first stage'"
            }
        }

        stage ('Second') {
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