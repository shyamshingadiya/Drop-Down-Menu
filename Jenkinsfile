pipeline {
  agent any
  stages {
    stage('Dev') {
      steps {
        build(job: 'BuildDev', propagate: true)
      }
    }
    stage('Unit Test') {
      steps {
        git(url: 'https://github.com/shyamshingadiya/Drop-Down-Menu/', branch: 'master', changelog: true)
      }
    }
  }
}