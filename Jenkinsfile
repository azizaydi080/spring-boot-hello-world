pipeline {
  agent any
  tools {
    // Installs Maven configured as "M398"
    maven "M398"
  }
  stages {
    stage('Echo Version') {
      steps {
        sh 'echo Print Maven Version'
        sh 'mvn -version'
      }
    }
    stage('Build') {
      steps {
        // Auto-checkout not yet enabled
     //   git 'http://139.84.159.194:5555/dasher-org/jenkins-hello-world.git'
        sh 'mvn clean package -DskipTests=true'
      }
    }
    stage('Unit Test') {
      steps {
        sh 'mvn test'
      }
    }
  }
}
