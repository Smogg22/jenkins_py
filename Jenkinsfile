pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
           	sh '''ls -la
		chmod 755 main.py'''
		sh './main.py'
		sh 'pylint main.py'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
           	sh '''ls -la
		chmod 755 main.py
		cp main.py /var/www/tls.server.fr/main.cgi''' 
	   }
        }
    }
}
