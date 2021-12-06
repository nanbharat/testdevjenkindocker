node {

def app 
 

 stage('Clone repository') {
     checkout scm
 }

  stage('Build image('example.app')') {
 app = docker.build()
 }


 stage('Push image') {
 app = docker.WithRegistry('https://registry.hub.docker.com','docker-hub-credentials')
 app.push('latest')
 }

}