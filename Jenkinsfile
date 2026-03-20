pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/andrew2002zhao/maven-samples.git', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh '''mvn clean
'''
        sh '''mvn test
'''
        sh 'mvn verify'
      }
    }

  }
  tools {
    maven 'default_maven'
    jdk 'java-17-openjdk'
  }
}
