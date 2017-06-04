node {
  stage('Checkout') {
    // checkout scm
    git url: 'https://github.com/PascalBourdier/testjenkins-hieradata.git', branch: 'master'
  }

  stage ('pwd') {
    sh 'pwd'
  }

  stage('Check syntax') {
    println "pwd".execute().text
    println "ls -la".execute().text
    println "yaml-lint .".execute().text
  }
}
