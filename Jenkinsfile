pipeline {
    agent none 
    stages {
        stage('Build') { 
            agent {
                label 'jenkins-02' 
                }
            }
            steps {
                sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
            }
        }
    }

