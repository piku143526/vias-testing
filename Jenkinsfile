node {
    stage('Checkout SCM') {
        git branch: 'main', url: 'https://github.com/piku143526/vias-testing.git'
    }
    stage("Build") {
      steps {
        sh "npm install"
         sh "ng lint"
          sh "npm start"
           sh "ng build"
      }
  
}
