pipeline {
    agent { docker { image 'node:14-alpine' } }
    environment {
        NAME = 'Emmy'
        SECRET_CREDENTIAL = credentials('secret-credential')
        SECRET_CREDENTIALS = credentials('secret-credentials')
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
                echo "You should never print: ${SECRET_CREDENTIAL}"
                echo "You also never print: ${SECRET_CREDENTIALS}, user: ${SECRET_CREDENTIALS_USR}, password: ${${SECRET_CREDENTIALS_PSW}}"
            }
        }
    }
}