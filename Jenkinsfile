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
                echo "doing build stuff.."
                '''
            }
        }
        stage('Test') {
            steps {
                echo "STAGE Testing.."
                sh '''
                echo "doing test stuff.."
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
