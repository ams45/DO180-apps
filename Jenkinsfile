
  pipeline {
    agent any
    environment {
             TEST_CRED = credentials('test-cred-id') 
    }
    stages {
        stage('Build') {
            
            steps {
                echo 'Building..'
                echo '$TEST_CRED'
                sh 'echo $TEST_CRED'
            }
        }
        stage('Test') {
            steps {
                //TEST_CRED = credentials('test-cred-id')
                echo 'Testing..'
                //echo '$TEST_CRED' 
                sh 'echo $TEST_CRED'
                sh "curl http://$TEST_CRED_USR:$TEST_CRED_PSW@scalar1.fyre.ibm.com:5984"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
    

