pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo \'Hi There\''
        sh 'mvn -B -DskipTests clean package'
      }
    }

  }
}