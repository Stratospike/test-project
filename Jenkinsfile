@Library('test-library@dev') _

pipeline {
    agent { label 'master' }

    environment {
        CRON_APP              = false
        AWS_ACCESS_KEY_ID     = "ak"
        AWS_SECRET_ACCESS_KEY = "sak"
        PROD_AWS_ACCESS_KEY_ID= "pak"
        PROD_AWS_SECRET_ACCESS_KEY = "psak"
    }

    stages {
        stage('build') {
            steps {
                ecsDeploy(applicationName: "myApp", version: "1234567890")
            }
        }
    }
}
