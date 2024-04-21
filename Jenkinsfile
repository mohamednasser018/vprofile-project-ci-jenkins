pipeline {
    agent any
    tools {
        maven "maven3"
        jdk "orcale_jdk_8"
    }
    environment {
        SNAP-REPO = 'vprofile-snapshot' 
        CENTRAL-REPO = 'vpro-maven-central'
        RELEASE-REPO = 'vprofile-release'
        NEXUS-GRP-REPO = 'vpro-maven-group'
        NEXUS-USER = 'admin'
        NEXUS-PASS = 'admin123'
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