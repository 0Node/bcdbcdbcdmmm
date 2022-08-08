pipeline {
    agent { 
        node {
            label 'linux'
            }
      }
      environment{
        AWS_DEFAULT_REGION="us-east-1"
      }
      triggers{
        pollSCM '*/5 * * * *'
      }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                aws --version
                aws ec2 describe-instances
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "doing test stuff.."
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}