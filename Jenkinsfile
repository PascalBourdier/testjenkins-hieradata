node {
  // Mark the code checkout 'stage'....
  stage('Checkout') {
    // Get some code from a GitHub repository
    checkout scm
  }

  stash includes: '*', name: 'all'

}

node {
  stage('Readme') {
    unstash 'all'
    def readme_md = readFile('README.md')
    echo readme_md
  }

  stage('yaml-lint') {
    unstash 'all'
    println "pwd".execute().text
    println "ls -la".execute().text
    println "yaml-lint .".execute().text
  }

}
