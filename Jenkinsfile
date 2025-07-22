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
