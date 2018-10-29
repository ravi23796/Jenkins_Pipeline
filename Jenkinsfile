pipeline {
    agent any
    stages {
        stage('Prerequisites') {
            steps {
                sh '''
                    cd /scratch/hgbu/chef-repo/cookbooks
                    pwd
                    whoami
                    knife client list
                '''
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }      
        stage('Step 4') {
            steps {
                sh 'echo "Step 5"'
            }
        }
        stage('Step 5') {
            steps {
                sh 'echo "Step 5"'
            }
        }
        
        stage('Step 6') {
            steps {
                sh 'echo "Step 6"'
            }
        }
        stage('Step 7') {
            steps {
                sh 'echo "Step 7"'
            }
        }
        stage('Step 8') {
            steps {
                sh 'echo "Step 8"'
            }
        }
        stage('Step 9') {
            steps {
                sh 'echo "Step 9"'
            }
        }
        stage('Step 10') {
            steps {
                sh 'echo "Step 10"'
            }
        }
        stage('Step 11') {
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
