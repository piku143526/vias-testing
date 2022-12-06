pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Git') {
      steps {
        git 'https://github.com/piku143526/vias-testing.git'
      }
    }
     
    stage('Build') {
      steps {
        sh 'npm install'
         sh 'ng build my-app -c production'
      }
    }  
    
            
    stage('Test') {
      steps {
        sh 'node test'
      }
    }
  }
}
