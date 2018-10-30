pipeline {
    agent any
    stages {
        stage('Prerequisites') {
            environment {
                SAMPLE = 'sample variable'
            }
            steps 
            {                
                    winRMClient credentialsId: 'OCMSLogin', hostName: 'llg00fgg.uk.oracle.com', winRMOperations: [invokeCommand('mkdir C:\\Monal')]                              
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
 
            slackSend channel: '#teamoffriends',
                  color: 'good',
                  message: "The pipeline ${currentBuild.fullDisplayName} completed successfully."
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
