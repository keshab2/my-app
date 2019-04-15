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
}


