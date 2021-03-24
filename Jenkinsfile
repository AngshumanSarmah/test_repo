pipeline {
    agent any

    stages {
        stage('Deploy') {
            when {
              expression {
                 echo "BUILD_ID 2" ${env.BUILD_ID}
                  
                currentBuild.result == null || currentBuild.result == 'SUCCESS' 
              }
            }
            steps {
                sh 'make publish'
            }
        }
    }
}
