pipeline {
  agent any
  stages {
    stage ('Build') {
      steps {
        echo 'Running build automation'
        script {
            if (isUnix()) {
                sh './gradlew build --no-daemon'
            }
            else {
                echo 'build in windows'
            }
        }
        // sh label: 'fuckinglabel', script: './gradlew build --no-daemon'
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}