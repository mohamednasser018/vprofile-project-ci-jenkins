pipeline {
    agent any
    tools {
        maven "maven3"
        jdk "orcale_jdk_8"
    }
    environment {
        SNAP_REPO = 'vprofile-snapshot' 
        CENTRAL_REPO = 'vpro-maven-central'
        RELEASE_REPO = 'vprofile-release'
        NEXUS-GRP_REPO = 'vpro-maven-group'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'admin123'
        NEXUSIP = '172.31.1.132'
        NEXUSPORT = '8081'
        NEXUS_LOGIN = 'nexuslogin'

    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn -s setting.xml -DskipTests install'
            }
        }
    }
}