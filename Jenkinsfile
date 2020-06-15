pipeline {
  agent any
  stages {
    stage('Build ') {
      steps {
        echo 'Starting of project'
      }
    }

    stage('Test') {
      steps {
        git(url: 'https://github.com/kudipudijahnavi/projectPIPE', branch: 'master', poll: true)
      }
    }

    stage('Artifacts') {
      steps {
        archiveArtifacts(artifacts: 'projectPIPE/target/*.jar', defaultExcludes: true, fingerprint: true, caseSensitive: true, allowEmptyArchive: true)
      }
    }

    stage('ending') {
      steps {
        echo 'end the piepline'
      }
    }

  }
}