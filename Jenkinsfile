node{
    stage('GIT Clone'){
        git 'https://github.com/ssharma2089/calcwebapp.git'
    }
    stage('Compile Package'){
        def mvnHome = tool name: 'Maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deploy to Tomcat'){ 
        sh 'cp target/*.war /opt/apache-tomcat-9.0.21/webapps'
    }    
}
