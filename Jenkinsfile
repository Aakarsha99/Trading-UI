pipeline {
    agent any
      

    stages {
        stage('Git checkout') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/Aakarsha99/Trading-UI.git'
                   }
}
        stage('Install npm prerequisites'){
            steps{
                sh 'echo runnning npm audit fix first command'
                sh'npm update'
                sh 'npm install'
                sh'npm run build'
                sh'cd /var/lib/jenkins/workspace/nodejs/build'
                sh'pm2 --name Trading-UI start npm -- start'
            }
        }
    }
}
