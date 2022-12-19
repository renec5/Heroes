node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarQubeScannerRene';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
      echo "SonarQube running"
    }
  }
}
