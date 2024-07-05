pipeline {
  agent any
  environment {
    pipelinedirectory = '/var/jenkins_home/workspace/globalbilgi-egitim-CI-CD-'
    branch = 'test'
  }
  stages {
    stage('update pipeline') {
      steps {
        script {
          sh "git -C ${env.pipelinedirectory} fetch"
          sh "git -C ${env.pipelinedirectory} checkout -b ${env.branch} origin/${env.branch}"
          sh "git -C ${env.pipelinedirectory} reset --hard origin/${env.branch}"
        }
      }
    }
  }
}