pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo \'Hi There\''
        sh 'mvn -B -DskipTests clean package'
      }
    }

    stage('Test') {
      agent any
      steps {
        sh 'mvn test'
        junit(testResults: 'target/surefire-reports/*.xml', allowEmptyResults: true)
      }
    }

  }
}