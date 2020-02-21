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
        
        stage('Jira test') {

            steps {
                 jiraDownloadAttachment file: 'https://jira-jenkins-test.atlassian.net/browse/AUT-1', id: 'BIDW', override: false, site: 'jira-jenkins-test.atlassian.net'
                }
            }

        stage('Deploy for QA') {
            when {
                  branch 'QA'
                  }
            steps {
                sh 'echo deploy QA'
                sh 'echo verify deploy to QA'
                }
            }
        }
     }
