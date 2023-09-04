node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    
    withSonarQubeEnv() {
      sh "/var/jenkins_home/maven/apache-maven-3.6.3/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=sonartest -Dsonar.projectName='sonartest'"
    }
  }
}
