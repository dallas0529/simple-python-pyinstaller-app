pipeline {
   agent {
      label 'jenkins-02'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
             }
            }
        }
    }

