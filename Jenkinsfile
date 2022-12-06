node {
    stage('Checkout SCM') {
        git branch: 'main', url: 'https://github.com/piku143526/vias-testing.git'
    }

    stage('Install node modules'){
        sh "npm install"
    }
 
    stage("Upgrade nodejs"){
        sh "apt-get install --only-upgrade nodejs"
    }
    stage("Start"){
        sh "npm start"
    }
    stage("Build"){
        sh "npm run build --prod"
    }
}
