node {
    stage('Checkout SCM') {
        git branch: 'main', url: 'https://github.com/piku143526/vias-testing.git'
    }

    stage('Install node modules'){
        sh "npm install"
    }
    env.NODEJS_HOME = "${tool 'NodeJsv12.16.2'}"
    env.PATH="${env.NODEJS_HOME}/bin:${env.PATH}"
    sh 'npm --version'

    stage('Preparation') { 
         
       }
    
    stages {
         stage('Build') {
              steps {
                 nodejs(nodeJSInstallationName: 'Node 6.x', configId: '<config-file-provider-id>') {
                    sh 'npm config ls'
                }
            }
        }
    }   
 }
