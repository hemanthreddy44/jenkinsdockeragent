pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Hello World"'
        sh 'python --version'
      }
    }

    stage('build_python') {
      steps {
        sh 'python hello.py'
        sh 'python hello.py > output.txt'
        sh 'cat output.txt'
        sh 'pwd'
        sh 'ls'
      }
    }

    stage('postBuild') {
      steps {
        sh 'echo "Hello World"'
        sh 'python --version'
        archiveArtifacts(allowEmptyArchive: true, artifacts: '\'/bitnami/jenkins/jenkins_home/workspace/jenkinsdockeragent_main/*.*\'')
      }
    }

  }
}