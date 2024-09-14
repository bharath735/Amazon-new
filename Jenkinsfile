pipeline {
    agent any
    stages {

        stage('pull') {
            steps {
                git branch: 'main', url: 'https://github.com/bharath735/Amazon-new.git'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('build') {
            steps {
                 sh 'mvn clean install'
            }
        }

        
    }

  post{

  success{
     echo 'Build Success'
  }
    
  failure{
       echo 'Failure in the build'
   }

  }


}
