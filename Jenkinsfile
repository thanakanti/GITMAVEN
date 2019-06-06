node {
  stage('SCM Checkout') {
        git 'https://github.com/rudrapdas82/GITMAVEN'
        }
   stage('Compile Project'){
     //Get MAVEN HOME PATH
     def mvnHome = tool name: 'maven-3', type: 'maven'
     sh "${mvnHome}/bin/mvn package"
       }
  stage('Email Notification'){
  mail bcc: '', body: '''Hi WELCOME TO JENKINS EMAIL ALERT
Thanks Rudra''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'rudrapdas82@gmail.com'
  }  
  stage('Slack Notification') {
    slackSend baseUrl: 'https://hooks.slack.com/services/', channel: 'jenkins-pipeline-demo', color: 'good', message: 'welcome to Jenkins slack!', teamDomain: 'RDDEVOPS', tokenCredentialId: 'slack-demo'
    
  }
}
