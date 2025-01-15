pipeline {
    agent any
       stages 
    {
        stage('checkout') {             
            steps {
                sh 'sleep 60'
                sh 'sudo su'
                sh 'cd /opt/apache-tomcat-10.1.34/webapps'
                sh 'curl -L -u "admin:cmVmdGtuOjAxOjE3NjgzOTI4MTA6OGRpUm1JdmZMSnFDNXhDOFRQSFVOV1dyNmxS" -O "http://23.20.102.242:8082/artifactory/hello-world-war-libs-release/com/efsavage/hello-world-war/1.0.20/hello-world-war-1.0.20.war"'
                sh 'pwd'
            }
        }
         
    }
}
