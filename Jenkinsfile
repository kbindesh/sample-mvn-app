pipeline {
  agent any

  tools {
    jdk 'Java-17'
    maven 'Maven-3.9.11'
  }

  stages{
    stage('Validate the code'){
      steps{
        sh 'mvn validate'
      }
    }
  }
}