def COLOR_MAP = [
    'FAILURE' : 'danger',
    'SUCCESS' : 'good'
]

pipeline 
{

    agent any

	tools {
        maven "maven3"
	    jdk "OracleJDK8"
    }

     environment {
        NEXUS_USER = 'admin'
        NEXUS_PASSWORD = 'admin'
        SNAP_REPO = 'vprofile-snapshot'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vprofile-central-repo'
        NEXUS_GRP_REPO = 'vprofile-grp-repo'
        NEXUS_IP = '127.0.0.1'
        NEXUS_PORT = '8081'
        NEXUS_LOGIN = "nexuslogin"

    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
     }
 }
