pipeline {
    agent { label 'prod' }

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'master', url: 'https://github.com/SunnyMahanth/Jenkins-A.git'
            }
        }
        stage('Deploy to Prod Server') {
            steps {
                sh 'scp -r * ubuntu@3.80.193.157:/var/www/html/'
            }
        }
    }
}
