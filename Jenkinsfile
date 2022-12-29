pipeline{
    agent any
    tools{
        maven MAVEN3
        jdk OracleJDK8
    }
    environment{
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'admin'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUSIP = '172.31.2.182'
        NEXUSPORT = '8081'
        NEXUS_LOGIN = 'nexuslogin'
    }
    stages{
        stage('BUILD'){
            steps{
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}