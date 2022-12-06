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
         sh 'ng lint'
          sh 'npm start'
           sh 'ng build'
      }
    }  
    
            
    stage('Test') {
      steps {
        sh 'node test'
      }
    }
  }
}
