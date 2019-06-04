node {
  stage('SCM Checkout') {
        git 'https://github.com/rudrapdas82/GITMAVEN'
        }
   stage('Compile Project'){
     def mvnHome = tool name: 'maven-3', type: 'maven'
     sh "${mvnHome}/bin/mvn package"
       }
}  
