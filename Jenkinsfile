pipeline {
  agent any
  tools {
    maven 'maven'
  }

  stages {
    stage('initialize') {
      steps {
        sh '''
          echo "PATH = ${PATH}"
          echo "M2_HOME = ${M2_HOME}"
          mvn --version
        '''
      }
    }

    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
  }
}
