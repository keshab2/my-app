  node{
   stage('SCM Checkout'){
     
     git 'https://github.com/keshab2/my-app'
        }
     stage('Compile-Package'){
       def mvnHome = tool name: 'maven-3', type: 'maven'
       sh "${mvnHome}/bin/mvn package"
          }
    stage('Slack Notification'){
         slackSend baseUrl: 'https://hooks.slack.com/services/',
          channel: '#jenkins-pipeline-demo',
          color: 'good', 
          message: 'Welcome to jenkins, Slack!', 
          teamDomain: 'javahomecloud', 
          tokenCredentialId: 'slack-demo'
    }
}


