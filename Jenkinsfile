node{
  def app
    stage('Clone') {
      checkout scm
    }
    stage('Build image') {
      app = docker.build("saidane/nginx")
    }
    stage('Run image') {
      docker.image('saidane/nginx').withRun('-p 81:81') { c ->
      sh 'docker ps'
      sh 'curl localhost'
    }
    }
} 
