pipeline {
  agent any

  stages {
    stage('Build') {
      when {
        branch 'master'
      }
      steps {
          echo 'Building stage started...'
          sh './gradlew build --no-daemon'
          archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
