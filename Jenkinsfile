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
        sh "docker build -t ${dockerImageTag} ."
      }
    }

    stage('Deploy Container To Openshift') {
      steps {
        sh "oc login https://localhost:8443 --username admin --password admin --insecure-skip-tls-verify=true"
        sh "oc project ${projectName} || oc new-project ${projectName}"
        sh "oc delete all --selector app=${projectName} || echo 'Unable to delete all previous openshift resources'"
        sh "oc new-app ${dockerImageTag} -l version=${version}"
        sh "docker run -p 5000:5000 ${dockerImageTag}"
      }
    }
  }
}
