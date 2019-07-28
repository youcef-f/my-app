node{
      
   stage('SCM Checkout'){
     git 'https://github.com/youcef-f/my-app.git'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'maven-3.5.0', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   } 
   stage('build docker image'){
      sh 'docker build -t youceff/my-app:2.0.0 .'
   } 
}
