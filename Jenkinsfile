pipeline {
    agent {
        label 'AGENT-1'
    }
    

    stages {
        stage('Build') {
           steps {
                sh 'echo This is Build'
                
            }
        }
        stage('Test') {
            steps {
               sh 'echo Testing..'
            }
        }
        stage('Deploy') {
            steps {
               sh 'echo Deploying....'
            }
        }
    }

 post {
        always{
            echo "This sections runs always"
            deleteDir()
            
        }
        success {
            echo "This section runs when pipeline success"
        }
        failure{
            echo "This section runs when pipeline failure"
        }
 }
}