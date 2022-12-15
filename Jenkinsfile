pipeline {
  agent any
    
    
  stages {
        
    stage('Git Checkout SCM') {
      steps {
         git 'https://github.com/piku143526/vias-testing.git'
      }
    }
     

    stage('Install node modules') {
        steps {
          sh 'npm install'
        }
    }

    stage('Build') {
       steps {
         sh 'ng build'
      }
    }  
    
    stage('Deploy') {
      steps {
        sh 'npm run build --prod'
      }
            
    }
  }
}
