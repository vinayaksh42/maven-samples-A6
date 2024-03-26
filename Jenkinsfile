pipeline {
  agent any
  stages {
    stage('git bisect') {
      steps {
        sh 'git bisect start 198644632661c67b6c32f59e9047c11a70685e15 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5'
      }
    }

    stage('git bisect run') {
      steps {
        sh 'git bisect run mvn clean test'
      }
    }

  }
  tools {
    maven 'Maven3.9.6'
    jdk 'Java11'
  }
}