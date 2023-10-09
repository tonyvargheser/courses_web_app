@Library('tony-shared-Lib') _

pipeline {
    agent any    
    tools{
        maven "Maven-3.9.4"
    }
    stages {
        stage('Clone') {
            steps {
		git 'https://github.com/tonyvargheser/courses_web_app.git'
             //git branch: 'main', credentialsId: 'GIT-CREDENTIALS', url: 'https://github.com/ashokitschool/courses_web_app.git'
            }
        }
        stage('Maven Build'){
            steps{
              mavenBuild()
            }
        }
		//stage('Code Review'){
			//steps{
				//sonarQube()
			//}
		//}
    }
}
