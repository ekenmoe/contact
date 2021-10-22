node{
  stage('SCM Checkout'){
  git 'https://github.com/ekenmoe/contact'
  }
  stage('Compile-Package'){
    // Get maven home path
   def mvnHome = tool name: 'M2_HOME', type: 'maven'
    sh "${mvnHome}/bin/mvn clean install package"
  }
}
