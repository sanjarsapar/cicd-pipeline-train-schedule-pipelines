pipeline{
    agent any
    stages {
        stage("Build") {
            steps{
                echo "Running build automation"
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
            post{
                always{
                    echo "====++++ always ++++===="
                }
                success{
                    echo "====++++ executed succesfully++++===="
                }
                failure{
                    echo "====++++ execution failed++++===="
                }

            }
        }
    }
}