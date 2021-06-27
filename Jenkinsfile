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

    stage('upload') {
      steps {
        sh 'ls -ltr'
      }
    }

    stage('deploy') {
      steps {
        sh 'scp target/petclinic.war root@10.0.5.204:/opt/tomcat/webapps/'
      }
    }

  }
}