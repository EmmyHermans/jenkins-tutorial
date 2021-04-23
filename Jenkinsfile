pipeline {
    agent { docker { image 'node:14-alpine' } }
    environment {
        NAME = 'Emmy'
    }
    stages {
        stage('build') {
            steps {
                sh 'npm --version'
                echo "Hello World, this is ${NAME}"
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}