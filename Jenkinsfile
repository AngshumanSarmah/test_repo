pipeline {
    agent any
    
    triggers {
       cron('TZ=Europe/London\n30 12 * * 1')
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Sending out emails'
            }
        }
    }
    post{
        always{
            emailext body: 'Hi, \nThis is a test', subject: 'Checking jenkinsfile', to: 'angshuman.sarmah@gmail.com'
        }
    }
}
