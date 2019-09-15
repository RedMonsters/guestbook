node {
   stage('Code checkout') { // for display purposes
      // Get some code from a GitHub repository
   checkout(git credentialsId: 'satyagit', url: 'https://github.com/st-tu-dresden/guestbook.git') 
   }
      stage('Build') {
     withMaven(jdk: 'Java', maven: 'Maven')   {
      sh 'mvn clean compile'
     } 
   }
   stage('Test') {
   withMaven(jdk: 'Java', maven: 'Maven')  {
      sh 'mvn test'
     }  
   }
  // stage('Sonar CodeAnalysis') {
   //  withSonarQubeEnv(credentialsId: 'sonar') { {
    //   sh 'mvn clean verify sonar:sonar'
     //     }

    }
   stage('Package') {
  withMaven(jdk: 'Java', maven: 'Maven') {
      sh 'mvn package'
     }  
   }
   
   
   stage('Artifactory') {
     
   }
   
   stage('Docker Build') {
     
   }
   
   stage('Deploy to Dev') {
     
   }
   stage('Deploy to Stage') {
     
   }
   stage('Deploy to Prod') {
     
   }
}
