node {
  stage('Checkout') {
    checkout scm
  }

  stage('Check syntax') {
    sh 'yaml-lint .'
  }
}
