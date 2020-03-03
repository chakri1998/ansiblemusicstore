node {
  stage('Git-Checkout') {
   git 'https://github.com/chakri1998/ansiblemusicstore.git'
  }
    
 def project_path="kalingamusic/"
 
 dir(project_path) {
    
  stage('Maven-Clean') {
   sh label: '', script: 'mvn clean'
  }
    
 stage('Maven-Compile') {
   sh label: '', script: 'mvn compile'
  }

   stage('Maven-Test') {
   sh label: '', script: 'mvn test'
  }
  
   stage('Maven-Package') {
   sh label: '', script: 'mvn package'
  }

   stage('Docker-Stage-Deployment') {
   sh label: '', script: 'docker-compose up -d --build'
  }
 }
}
