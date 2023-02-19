pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG20CS151_task5 PES2UG20CS151_task5.cpp'
                build job: 'PES2UG20CS151-1'
            }
        }
        
        stage('Test') {
            steps {
                sh './PES2UG20CS151_task5'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deployment'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
