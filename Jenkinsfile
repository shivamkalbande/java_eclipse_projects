pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building Java Project'
        bat 'bat \'.\\mvnw clean compile\''
        git(url: 'git@github.com:shivamkalbande/java_projects.git', credentialsId: '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', branch: 'master')
      }
    }

    stage('test') {
      steps {
        echo 'Tested on windows'
      }
    }

    stage('Deploy Staged') {
      steps {
        echo 'Added to deploy stageing'
        input 'Is ok to deploy to production???'
      }
    }

    stage('Deploy to Production') {
      steps {
        echo 'Ready to Production'
      }
    }

  }
}