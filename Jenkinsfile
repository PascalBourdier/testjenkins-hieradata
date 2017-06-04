node {
  //stage('Checkout') {
  //  checkout scm
  //}

  stage('Check syntax') {
    ansiColor('xterm') {
      sh 'yaml-lint -i .'
    }
  }
}
