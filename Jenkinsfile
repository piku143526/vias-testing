node {
    stage('Checkout SCM') {
        git branch: 'main', url: 'https://github.com/piku143526/vias-testing.git'
    }

    env.NODEJS_HOME = "${tool 'NodeJsv18.12.1'}"
    env.PATH="${env.NODEJS_HOME}/bin:${env.PATH}"
    sh 'npm --version'

    stage('Preparation') { 
         
       }
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
