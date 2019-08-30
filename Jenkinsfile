node {
  stage('Preparation') {
     git 'https://github.com/dazaykov/spring-petclinic.git'
  }
  stage('Build') {
     sh ''./mvnw -Dmaven.test.failure.ignore verify'
  }
  stage('Results') {
     junit '**/target/surefire-reports/TEST-*.xml'
     archiveArtifacts 'target/*.jar'
  }
}
