pipeline{
    agent any
        tools{
            maven "MAVEN3"
            jdk "OracleJDK8"
        }
        environment{
            SNAP-REPO = 'vprofile-snapshot'
            NEXUS-USER = 'admin'
            NEXUS-PASS = 'admin'
            RELEASE-REPO = 'vprofile-release'
            CENTRAL-REPO = 'vpro-maven-central'
            NEXUS-GRP-REPO = 'vpro-maven-group'
            NEXUSIP = '172.31.7.115'
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