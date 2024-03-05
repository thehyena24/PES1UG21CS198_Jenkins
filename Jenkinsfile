pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "This is Build stage."
                build 'PES1UG21CS198-1'
                sh 'g++ ./main/hello.cpp -o output'
                echo "Build Stage Successful"
            }
        }
        stage('Test') { 
            steps {
                echo "This is Test stage." 
                sh './output'
                echo "Test Stage Successful"
            }
        }
        stage('Deploy') { 
            steps {
                ech "This is Deploy stage."
                echo "Deployment Success"
            }
        }
    }
    post{
        failure{
            error 'Pipeline Failed'
        }
    }
}
