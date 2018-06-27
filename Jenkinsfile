pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000 -v /var/run/docker.sock:/var/run/docker.sock' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'docker build . -t registry.cn-beijing.aliyuncs.com/rdc-template/repo:110' 
            }
        }
    }
}
