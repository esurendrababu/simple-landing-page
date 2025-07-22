pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/esurendrababu/simple-landing-page.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Make sure Apache is installed and running on the VM
                    sh 'sudo -i'
                    sh 'rm -rf /var/www/html/*'
                    sh 'cp -r * /var/www/html/'
                    echo 'Deployment to Apache successful'
                }
            }
        }
    }
}
