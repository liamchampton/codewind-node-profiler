#!groovy​
pipeline {
    agent any

	 options {
        timestamps()
        skipStagesAfterUnstable()
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
				sh '''
					npm install
					npm install -g vsce
					vsce package
					echo "Extension build complete"
					ls -la
				'''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}