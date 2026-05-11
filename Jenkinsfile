pipeline{
	agent any
	tools{
		gradle 'Gradle'
	}
	stages{
		stage('Checkout'){
			steps{
				git branch: 'main' ,url : 'https://github.com/puneethagowda16/devopstest2.git'
			}
		}
		stage('build'){
			steps{
				sh './gradlew build'
			}
		}
		stage('test'){
			steps{
				sh 'gradle test'
			}
		}
		stage('deploy'){
			steps{
				sh 'gradle run'
				sh 'gradle display'
			}
		}
	}
	post{
		success{
			echo 'Build and deployment successful'
		}
		failure{
			echo 'Build Failure'
		}
	}
}
