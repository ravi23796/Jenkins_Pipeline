pipeline {
    agent any
    stages {
        stage('Prerequisites') {
            environment {
                SAMPLE = 'sample variable'
            }
            steps {
                bat '''
                    cd C:\\chef
                    knife client list
                    echo %SAMPLE%
                '''                
            }
        }             
        }            
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
            mail to: 'ravi.al.kumar@oracle.com',
             subject: "Pipeline: ${currentBuild.fullDisplayName}",
             body: "Pipeline ${env.BUILD_URL} completed successfully" 
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}    
