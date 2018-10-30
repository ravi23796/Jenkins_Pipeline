pipeline 
{
    agent any
    stages 
    {
        stage('Prerequisites') 
        {
            environment 
            {
                SAMPLE = 'sample variable'
            }
            steps 
            {
                bat '''
                    cd C:\\chef\\cookbooks
                    chef generate cookbook pipeline
                    knife cookbook upload pipeline
                    echo %SAMPLE%
                '''                
            }
        }
        stage('4.Uploading Databag') 
        {
            steps 
            {
                bat 'echo "Step 5"'                
            }
        }
        stage('5.Vault Installation') 
        {
            steps 
            {
                bat 'echo "Step 5"'
            }
        }
        
        stage('6.OCMS Prerequisites') 
        {
            steps 
            {
                bat 'echo "Step 6"'
            }
        }
        stage('7.DB Installation') 
        {
            steps 
            {
                bat 'echo "Step 7"'
            }
        }
        stage('8.MI Domain Creation') 
        {
            steps 
            {
                bat 'echo "Step 8"'
            }
        }
        stage('9.Starting Servers') 
        {
            steps 
            {
                bat 'echo "Step 9"'
            }
        }
        stage('10.OCMS Deployments') 
        {
            steps 
            {
                bat 'echo "Step 10"'
            }
        }
        stage('11.Restarting All Servers') 
        {
            steps 
            {
                bat 'echo "Step 11"'
            }
        }
    }            
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'            
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
