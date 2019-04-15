  node{
   stage('SCM Checkout'){
      git 'https://github.com/keshab2/my-app'
        }
     stage('Compile-Package'){
       //Get maven home path
       def mvnHome = tool name: 'maven-3', type: 'maven'
       sh "${mvnHome}/bin/mvn package"
    }
    stage('Email Notification'){
    mail bcc: '', body: '''Hi Welcome to jenkins email alerts
Thanks
Keshab''', cc: '', from: '', replyTo: '', subject: 'Jenkins Jobs', to: 'keshabkumar8@gmail.com'
    }
    stage ('Slack Notification') {
      slackSend baseUrl: 'https://hooks.slack.com/services/',
        channel: '#jenkins-pipelinedemo1', 
        color: 'good', 
        message: 'Welcome to Jenkins, Slack1!', 
        teamDomain: 'nttdata-ztd1876.slack.com', 
        tokenCredentialId: 'slack-demo'
    }
}


