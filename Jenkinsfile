pipeline {
    agent { 
        node {
            label 'docker-agent-python'
            }
      }
    triggers {
        pollSCM '* * * * * ' /* every minute */
      }
    stages {
        stage('Build') {
            steps {
                echo "STAGE Building.."
                sh '''
                pip install -r requirements.txt
                '''
            }
        }
        stage('Test') {
            steps {
                echo "STAGE Testing.."
                sh '''
                python3 hello.py
                python3 hello.py --name="Tsuki"
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'STAGE Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
