pipeline {
  agent any
  stages {
    stage('Dev') {
      steps {
        build(job: 'BuildDev', propagate: true)
      }
    }
    stage('Unit Test') {
      parallel {
        stage('Unit Test') {
          steps {
            build 'QA'
          }
        }
        stage('') {
          steps {
            build 'Sears_QA'
          }
        }
        stage('') {
          steps {
            build 'SHC_QA'
          }
        }
      }
    }
  }
}