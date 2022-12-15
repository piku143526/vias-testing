pipeline {
  agent any
    
    
  stages {
        
    stage('Git Checkout SCM') {
      steps {
         git url: 'https://github.com/piku143526/vias-testing.git', branch: 'main'
                // Change file permisson
                sh "chmod +x -R ./jenkins"
                // Run shell script
                sh "./jenkins/script/scripted_pipeline_ex_2.sh"
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
