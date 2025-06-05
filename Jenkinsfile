pipeline {
    agent { label 'test' }

    stages {
        stage('Clone Repo') {
            steps {
                git branch: 'test', url: 'https://github.com/SunnyMahanth/Jenkins-A.git'
            }
        }
        stage('Deploy to Test Server') {
            steps {
                sh 'scp -r * ubuntu@<test-server-ip>:/var/www/html/'
            }
        }
    }
}
