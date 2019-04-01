pipeline {
    agent {
        label 'jenkins-01'
    }
    stages {
        stage('Build') {
            steps {
                sh 'python3 -m py_compile sources/add2vals.py sources/calc.py' 
            }
        }
    }
}
