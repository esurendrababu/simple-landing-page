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
            sh '''
                echo "Deploying to Apache..."
                sudo rm -rf /var/www/html/*
                sudo cp -r * /var/www/html/
                echo "Deployment successful!"
            '''
        }
    }
}

    }
}
