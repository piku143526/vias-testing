node {
    stage('Checkout SCM') {
        git branch: 'main', url: 'https://github.com/piku143526/vias-testing.git'
    }

    stage('Install node modules'){
        sh "npm install"
    }
    stage("Test"){
        sh "npm run test-headless"
    }
    stage("Build"){
        sh "npm run build --prod"
    }
}
