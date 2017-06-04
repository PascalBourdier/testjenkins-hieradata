node {
  // Mark the code checkout 'stage'....
  stage('Checkout') {
    // Get some code from a GitHub repository
    checkout scm
  }

  stash includes: '*', name: 'readme'

}

node {
  stage('Readme') {
    unstash 'readme'
    def readme_md = readFile('README.md')
    echo readme_md
  }
}
