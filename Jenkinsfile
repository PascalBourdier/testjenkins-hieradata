node {
  // Mark the code checkout 'stage'....
  stage('Checkout') {
    // Get some code from a GitHub repository
    checkout scm
  }

  stash includes: '*', name: 'all'

}

node {
  unstash 'all'

  stage('Readme') {
    def readme_md = readFile('README.md')
    echo readme_md
  }

  stage('yaml-lint') {
    println "pwd".execute().text
    println "ls -la".execute().text
    println "yaml-lint .".execute().text
  }

}
