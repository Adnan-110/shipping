pipeline{
    agent{
        label 'ws'
    }
    stages{
        stage('Lint Checks') {
            steps {
                sh "echo ****** Starting Style Checks ****** "
                sh "mvn checkstyle:check || true"
                sh "echo ****** Style Check are Completed ******"
            }
        }
        stage('Static Code Analysis') {
            steps{
                sh "echo ****** Starting Static Code Analysis ******"
            }   
        }
    }
}