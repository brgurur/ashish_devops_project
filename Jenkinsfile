pipeline {
    agent any
	  tools {
        'org.jenkinsci.plugins.docker.commons.tools.DockerTool' '18.09'
		}

    stages {
		stage('Git Cloe Repo.......') {
		
            steps {
                git branch: 'main', credentialsId: 'ba283931-f9ad-4318-a410-a2dcfb4e08f0', url: 'https://github.com/brgurur/ashish_devops_project.git'
			}
        
		}
        stage('Build.............') {
            steps {
                echo 'Building..'
				sh "docker version" 
				sh "docker-compose version" 
				sh "cd kafka_zookeeper && docker-compose --file kafka_zookeeperdocker-compose-kafka-zookeeper.yaml up -d"
            }
        }
        stage('Test......') {
            steps {
                echo 'Testing..'
				bat 'docker images'
				bat 'docker ps -a'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}