node {
 stage('SCM') {
 git branch: 'main', credentialsId: 'testing-github', url: 'https://github.com/SeRi0720/oop-bee.git'
 }
 stage('SonarQube Analysis') {
 def scannerHome = tool 'SonarQube Scanner';
 withSonarQubeEnv() {
 sh "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=. -Dsonar.projectKey=oop-bee -Dsonar.login=sqa_7983a285c251281605728c79f340b9bda105c584"
   }
  }
}
