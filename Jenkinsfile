node {
  stage('Checkout') {
    checkout scm
  }

  stage('Check syntax') {
    unstash 'all'
    println "pwd".execute().text
    println "ls -la".execute().text
    println "yaml-lint .".execute().text
  }
}
