pipeline{
  agent any
stages{
stage('git checkout scm'){
  steps{
git 'https://github.com/atulrockzz/mvn_sonar.git'
     }
}
  stage('Analysis'){
    steps{
    sh '/opt/Maven/bin/mvn clean verify sonar:sonar -Dsonar.password=admin -Dsonar.login=admin'
  }
  }
  stage('Build'){
    steps{
      sh '/opt/Maven/bin/mvn clean install'
    }
  }
}
}
  
 
