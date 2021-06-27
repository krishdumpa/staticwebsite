pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'git@github.com:krishdumpa/staticwebsite.git', branch: 'develop')
      }
    }

    stage('build') {
      steps {
        sh '/opt/maven38/bin/mvn clean package '
      }
    }
