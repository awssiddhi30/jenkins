pipeline {
    agent {
        label 'AGENT-1'
    }
    options{
         timeout(time: 10, unit: 'SECONDS')
    }
    

    stages {
        stage('Build') {
           steps {
                sh 'echo This is Build'
                sh 'sleep 10'
                
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