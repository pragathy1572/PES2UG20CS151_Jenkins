pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ temp.cpp -o temp'
                 build job: 'PES2UG20CS151-1', wait: false
                 echo 'Build by CS151 successful'
            }
        }

        stage('Test') {
            steps {
                sh 'cat temp.cpp'
                echo 'Test by CS151 successful'
            }
        }

        stage('Deploy') {
            steps {
               
                echo 'Deploy by CS151 successful'
            }
        }
    }

    post {
        failure {
           
                echo 'Pipeline Failed'
         
        }
    }
}
