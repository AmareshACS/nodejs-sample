pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh "npm install"
                sh "npm run build -if-present"
            }
        }
       stage('deploy') {
            steps {
                sh "rm -rf  /var/www/node-app/*"
                sh "cp helloworld.js /var/www/node-app"
                sh "node /var/www/node-app/helloworld.js &"
            }
        }
    }
}
