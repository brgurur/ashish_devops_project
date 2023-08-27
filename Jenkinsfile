pipeline {
    agent any

    stages {
		stage('Git Cloe Repo.......') {
		
            steps {
                git branch: 'main', credentialsId: 'ba283931-f9ad-4318-a410-a2dcfb4e08f0', url: 'https://github.com/brgurur/ashish_devops_project.git'
				bat 'python test.py'
            }
        
		}
        stage('Build') {
            steps {
                echo 'Building..'
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