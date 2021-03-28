node('java'){
    stage('Git-CheckOut') {
        echo 'Checking out from Git Repo!!!'
        git credentialsId: '4b39526e-26f9-4e8f-ad69-0e4e9c34de0b', url: 'http://localhost:5000/gitserver/butler/pipeline-demo.git'
    }
    stage('Build') {
        echo 'Building the check out repository'
        sh './jenkins/build.sh'
    }
    stage('Test') {
        echo 'Testing'
        sh './jenkins/test-all.sh'
    }
    stage('Build') {
        echo 'Deploying'
        sh './jenkins/deploy.sh'
    }
}
