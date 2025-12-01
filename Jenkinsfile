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
    stage('Reviewing the code'){
      steps{
        sh 'mvn verify sonar:sonar -Dsonar.projectKey=mvnapp-org_mvn-project -Dsonar.organization=mvnapp-org -Dsonar.projectName=mvn-project -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=e73c690dc0241b732b0d3509a6312fe750c91e41 -X'
      }
    }
  }
}