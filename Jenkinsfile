pipeline {
    agent any

    stages {
        stage('Deploy') {
            when {
              expression {
                 echo "currentBuild 1" currentBuild
                 echo "currentBuild 2" %currentBuild%
                  
                currentBuild.result == null || currentBuild.result == 'SUCCESS' 
              }
            }
            steps {
                sh 'make publish'
            }
        }
    }
}
