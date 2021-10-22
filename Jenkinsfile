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
    color: 'good', message: 'MAA OO, Je viens chez toi quant on part au champ a manigotant, hahahaha!', 
    tokenCredentialId: 'slack-demo', 
    username: 'incoming-webhook'
  }
}
