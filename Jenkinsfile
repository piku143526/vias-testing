node {
    stage('Checkout SCM') {
        git branch: 'main', url: 'https://github.com/piku143526/vias-testing.git'
    }
    stage("Install node modules"){
        sh "npm install"
    }
    stage("Build"){
        sh "ng build"
    }
      
    stage("watch"){
        sh "ng build --watch --configuration development"
    }    
    stage("test"){
        sh "ng test"
      
    }
  
}
