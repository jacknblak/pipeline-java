pipeline {
    agent any 

    stages {
        stage ('pull'){
            steps {
                sh 'echo this is pulling stage'
            }
        }
        stage ('build') {
            steps {
                sh 'echo Compiling source code'
            }
        }
        stage ('deployment') {
            steps {
                sh 'echo Deployment started...'
                sh 'sleep 20'
            }
        }

        post {
            always {
                emailext {
                subject:${env.JOBNAME} IS SUCCESSFUL!!!!
                to: saravanaprabu@hpe.com
                }
            }
        }
    }
}

