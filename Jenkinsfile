pipeline {
    agent any
    stages {
        stage('Prerequisites') {
            environment {
                SAMPLE = 'sample variable'
            }
            steps {
                sh '''
                    cd /scratch/hgbu/chef-repo/cookbooks
                    pwd
                    whoami
                    knife client list
                    echo $SAMPLE
                '''
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }      
        stage('4.Uploading Databag') {
            steps {
                sh 'echo "Step 5"'
            }
        }
        stage('5.Vault Installation') {
            steps {
                sh 'echo "Step 5"'
            }
        }
        
        stage('6.OCMS Prerequisites') {
            steps {
                sh 'echo "Step 6"'
            }
        }
        stage('7.DB Installation') {
            steps {
                sh 'echo "Step 7"'
            }
        }
        stage('8.MI Domain Creation') {
            steps {
                sh 'echo "Step 8"'
            }
        }
        stage('9.Starting Servers') {
            steps {
                sh 'echo "Step 9"'
            }
        }
        stage('10.OCMS Deployments') {
            steps {
                sh 'echo "Step 10"'
            }
        }
        stage('11.Restarting All Servers') {
            steps {
                sh 'echo "Step 11"'
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
