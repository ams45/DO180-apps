
  pipeline {
    agent any

    stages {
        stage('Build') {
            environment {
             TEST_CRED = credentials('test-cred-id') 
            }
            steps {
                echo 'Building..'
                echo '$TEST_CRED'
                sh 'echo $TEST_CRED'
            }
        }
        stage('Test') {
            steps {
                TEST_CRED = credentials('test-cred-id')
                echo 'Testing..'
                echo '$TEST_CRED' 
                sh 'echo $TEST_CRED'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
    

