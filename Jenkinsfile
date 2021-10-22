node{
  stage('SCM Checkout'){
  git 'https://github.com/ekenmoe/contact'
  }
  stage('Compile-Package'){
  sh 'mvn package'
  }
}
