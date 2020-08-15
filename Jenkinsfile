pipeline {
  agent any
  triggers {
      githubPush()
  }
  stages {
    stage ('Build') {
      steps {
        echo 'Running build automation'
        script {
            // if (isUnix()) {
            //     sh './gradlew build --no-daemon'
            // }
            // else {
            //     echo 'build in windows'
            sh label: 'fuckinglabel', script: './gradlew build --no-daemon'
            // }
        } // #TEMP
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
// // //