node {
    stage('Checkout SCM') {
        git branch: 'main', url: 'https://github.com/piku143526/vias-testing.git'
    }
    
  pipeline {
    agent any

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
}
