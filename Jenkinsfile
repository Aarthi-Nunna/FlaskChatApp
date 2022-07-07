def projectName = 'pipelinechatapp'
def version = "0.0.${currentBuild.number}"
def dockerImageTag = 'pipelinechatapp'

pipeline {
  agent any

  stages {
    stage('Test') {
      steps {
        echo 'testing'
      }
    }

    stage('Build') {
      steps {
        echo 'building'
      }
    }

    stage('Build Container') {
      steps {
        bat "docker build -t ${dockerImageTag} ."
      }
    }

    stage('Deploy Container To Openshift') {
      steps {
        bat "docker run -it -p 5000:5000 ${dockerImageTag}"
      }
    }
  }
}
