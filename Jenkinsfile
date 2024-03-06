pipeline{
    agent any
        stages{
            stage('Build'){
                steps{
                    build 'PES1UG21CS584_1'
                    sh 'g++ main.cpp -o output'
                }
            }
            stage('Test'){
                steps{
                    sh './output'
                }
            }
            stage('Deploy'){
                steps{
                    echo 'Deployment Successful'
                }
            }
        }
        post {
            failure{
                echo 'Pipeline failed'
            }
        }
}
