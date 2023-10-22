pipeline {
    agent { 
        node {
            label 'dockertest'
            }
      }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
               echo "doing Building.."
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                echo "doing Testing.."
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
    post {
        success {
            script {
                slackSend(channel: "my_first_jenkins_pipelines", message: "my_first_jenkins_pipelines passed successfully")
                    }
                }
        failure {
            script {
                slackSend(channel: "my_first_jenkins_pipelines", message: "my_first_jenkins_pipelines Falied ")
                    }
                }
            }
}
