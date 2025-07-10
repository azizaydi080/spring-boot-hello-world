pipeline {
  agent any
  stages {
    stage('Echo Version') {
      steps {
        sh 'echo Print Maven Version'
        sh 'mvn -version'
      }
    }

    stage('Build') {
      steps {
        sh 'mvn clean package -DskipTests=true'
        archiveArtifacts 'spring-boot-2-hello-world-*.jar'
      }
    }

    stage('Unit Test') {
      steps {
        sh 'mvn test'
      }
    }

  }
  tools {
    maven 'M398'
  }
}