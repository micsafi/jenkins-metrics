pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'echo Running build.'
            }
        }
    }
    post {
      always {
        influxDbPublisher(selectedTarget: 'jenkins-metrics')
      }
    }
}
