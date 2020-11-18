@Library('piper-lib-os@helloWorld') _

node() {
  stage('init') {
    deleteDir()
  }
  stage('prepare piper') {
    dockerExecuteOnKubernetes(script: this, dockerImage: 'golang:1.15') {
      sh "echo hello; whoami; ls -la; pwd; which git"
    }
  }
  stage('Hello World') {
      helloWorld script: this
  }
}
