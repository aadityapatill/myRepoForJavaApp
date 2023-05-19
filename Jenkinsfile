pipeline {
    agent any

    stages {
        
        stage ("Build") {
            steps {
                sh "mvn clean install -f MyWebApp/pom.xml"
            }
        }
        
        stage ("Code scan") {
            steps {
            }
        }
        
        stage ("code coverage") {
            steps {
            }
        }
        
        stage ("Binary Upload") {
            steps {
nexusArtifactUploader artifacts: [[artifactId: 'MyWebApp', classifier: '', file: 'target/MyWebApp-1.0.war', type: 'war']], credentialsId: 'NEXUS', groupId: 'com.mkyong', nexusUrl: 'http://localhost:8081/', nexusVersion: 'nexus3', protocol: 'http', repository: 'http://localhost:8081/repository/Qapitol/', version: '1.0-SNAPSHOT'            }
        }
}
