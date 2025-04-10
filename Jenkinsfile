
r'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts artifacts: 'target/*.jar', followSymlinks: false, onlyIfSuccessful: true
      }
    }

  }

  post {
    always {
      junit(
        allowEmptyResults: true,
        testResults: 'target/surefire-reports/*.xml'
      )
    }
  }


}






