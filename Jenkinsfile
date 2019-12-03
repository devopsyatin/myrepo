pipeline {
    agent any

    stages {
        stage('initializing') {
            steps {
                
            sh 'echo initializing'
                  }
        }

        stage('deploy to testenv') {

            steps {
                 sh 'echo deploy to testenv'
                }
            }


        stage('Deploy for QA') {
            when {
                  branch 'QA'
                  }
            steps {
                sh 'echo deploy QA'
                }
            steps {
                sh 'echo verify QA'
                  }
            }
        }
     }
