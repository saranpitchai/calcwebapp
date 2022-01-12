node{
    stage('Git Clone'){
        git 'https://github.com/saranpitchai/calcwebapp.git'
    }
    stage('Maven Package'){
        def mvnHome = tool name: 'mvn', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deployment'){ 
        sh 'cp target/*.war /opt/tomcat/webapps'
    }    
}
