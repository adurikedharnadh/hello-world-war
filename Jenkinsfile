pipeline {
    agent any
       stages 
    {
        stage('checkout') {             
            steps {
                sh """
                #!/bin/bash
                sleep 60
                sudo su
                cd /opt/apache-tomcat-10.1.34/webapps
                ls
                curl -L -u "admin:cmVmdGtuOjAxOjE3NjgzOTI4MTA6OGRpUm1JdmZMSnFDNXhDOFRQSFVOV1dyNmxS" -O "http://3.94.159.27:8082/artifactory/hello-world-war-libs-release/com/efsavage/hello-world-war/1.0.24/hello-world-war-1.0.24.war"
                pwd
                cd /opt/apache-tomcat-10.1.34/bin
                ./shutdown
                cd /opt/apache-tomcat-10.1.34/bin
                ./startup.sh
                """ 

            }
        }
         
    }
}
