@Library('tony-shared-Lib) _

pipeline {
    agent any    
    tools{
        maven "Maven-3.9.4"
    }
    stages {
        stage('Clone') {
            steps {
             git branch: 'main', credentialsId: 'Git-Credentials', url: 'https://github.com/ashokitschool/courses_web_app.git'            }
        }
        stage('Maven Build'){
            steps{
              mavenBuild()
            }
        }
		
    }
}
