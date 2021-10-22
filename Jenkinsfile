node{
  stage('SCM Checkout'){
  git 'https://github.com/ekenmoe/contact'
  }
  stage('Compile-Package'){
    // Get maven home path
   def mvnHome = tool name: 'M2_HOME', type: 'maven'
    sh "${mvnHome}/bin/mvn clean install package"
  }
  stage('Slack Notification'){
  slackSend baseUrl: 'https://hooks.slack.com/services/', 
    channel: 'app-support-jenkins-demo', 
    color: 'good', message: 'Welcome to jenkins slack!', 
    tokenCredentialId: 'slack-demo', 
    username: 'incoming-webhook'
  }
}
