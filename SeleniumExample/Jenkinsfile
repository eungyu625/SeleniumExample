pipeline {
    agent {
        label "demoAgent"
    }
    stages {
        stage('git') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'master', url: 'https://github.com/eungyu625/SeleniumExample.git'
            }
        }
        stage('mvn') {
            steps {
                // Run Maven on a Unix agent.
                sh "mvn -Dmaven.test.failure.ignore=true clean test"
            }
        }
    }
}