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
					npm install npx
					npm install vsce
					ls -la
					#npx vsce package
					#vsce package
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