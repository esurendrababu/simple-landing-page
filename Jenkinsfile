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
                    // Assumes Apache is already installed and running
                    sh '''
                        sudo rm -rf /var/www/html/*
                        sudo cp -r * /var/www/html/
                        echo "Deployment to Apache successful"
                    '''
                }
            }
        }
    }
}
