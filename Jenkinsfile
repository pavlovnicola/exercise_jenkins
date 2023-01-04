pipeline {
	agent none
	stages {
		stage('Run 1') {
		    agent {
		        dockerfile {
		            filename 'Dockerfile-python'
		            args '-v /tmp:/tmp'
		        }
		    }
			steps {
				sh 'python3 --version'
				sh 'python3 main.py'
			}
		}
		stage('Run 2') {
		    agent {
		        kubernetes {
		            idleMinutes 5
		            yamlFile 'build-pod.yaml'
		            defaultContainer 'docker'
		            namespace 'kubernetes-plugin'
		        }
		    }
			steps {
			    container('docker') {
    				sh 'python3 --version'
    				sh 'python3 main.py'
			    }
			}
		}
	}
}
