node {
 stage('SCM') {
 git branch: 'main', credentialsId: 'testing-github', url: 'https://github.com/SeRi0720/oop-bee.git'
 }
 stage('SonarQube Analysis') {
 def scannerHome = tool 'SonarQube Scanner';
 withSonarQubeEnv() {
 sh "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=. -Dsonar.projectKey=oop-bee -Dsonar.login=sqa_e380793904b17cd948c7796d53f8467d6461f3f4"
   }
  }
}
