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
        stage('4.Uploading Databag') {
            steps {                
            }
        }
        stage('5.Vault Installation') {
            steps {                
            }
        }
        
        stage('6.OCMS Prerequisites') {
            steps {                
            }
        }
        stage('7.DB Installation') {
            steps {                
            }
        }
        stage('8.MI Domain Creation') {
            steps {                
            }
        }
        stage('9.Starting Servers') {
            steps {                
            }
        }
        stage('10.OCMS Deployments') {
            steps {                
            }
        }
        stage('11.Restarting All Servers') {
            steps {                
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
