pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    environment {
      SNAP_REPO = 'vpro-snapshot'
      NEXUS_USER = 'admin'
      NEXUS_PASS = 'nadhouraadmin'
      RELEASE_REPO = 'vpro-release'
      CENTRAL_REPO = 'vpro-maven-central'
      NEXUS_IP = '172.31.83.70'
      NEXUS_PORT = '8081'
      NEXUS_GRP_REPO = 'vpro-maven-group'
      NEXUS_LOGIN = 'nexuslogin'

    }
    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}