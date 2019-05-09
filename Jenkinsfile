  node{
    stage('SCM Checkout'){
      def mvnHome =   tool name: 'maven-3', type: 'maven'
      git 'https://github.com/keshab2/my-app'
     }
     stage('Compile-Package'){
       def mvnHome =   tool name: 'maven-3', type: 'maven'
       sh "${mvnHome}/bin/mvn package"
    }
 
  }

