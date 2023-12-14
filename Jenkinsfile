pipeline{
    agent{
        label 'ws'
    }
    tools{  // This option will make build tools available only for this single run and will not install permanently.
        maven 'maven-390' // In This way we configured in Jenkins->mangage->Tools section that whenever maven-390 is passed make maven-3.9.0 version available
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