pipeline{
	agent any
	tools{
		maven 'Maven-3.9.9'
	}
	stages{
		stage("Build"){
			steps{
				echo "========Building========"
				sh 'mvn clean install'
			}
		stage('Test'){
			steps{
				echo "========Testing========="
				sh 'mvn test'
			}
		}
			post{
				always{
					echo "========always========"
				}
				success{
					echo "========A executed successfully========"
				}
				failure{
					echo "========A execution failed========"
				}
			}
		}
	}
}
