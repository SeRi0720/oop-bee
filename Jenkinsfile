node {
 stage('SCM') {
 git branch: 'main', credentialsId: 'testing-github', url: 'https://github.com/SeRi0720/oop-bee.git'
 }
 stage('SonarQube Analysis') {
 def scannerHome = tool 'SonarQube Scanner';
 withSonarQubeEnv() {
 sh "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=. -Dsonar.projectKey=oop-bee -Dsonar.login=sqa_1194c0e62c5ae5697f46c1574177f11142531f5e"
   }
  }
}
