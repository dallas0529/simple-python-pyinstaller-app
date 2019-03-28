pipeline {
    agent {
      label 'jenkins-01'
    }
    stages {
        stage('checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'b70ca99a-4721-451c-a560-2fa8bcce1640', url: 'https://github.com/dallas0529/simple-python-pyinstaller-app.git']]])
            }
        }
        stage('build') { 
            steps {
                cmakeBuild buildDir: 'build', installation: 'InSearchPath'
            }
        }
        stage('test') {
            steps {
                ctest arguments: '-v', installation: 'InSearchPath', workingDir: 'build'
            }
        }
    }
}
