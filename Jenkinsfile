pipeline {
    agent any
    environment {
       Sample_creds = credentials('Jfrog')
    }
       stages 
    {
        stage('Waiting for stage CI to complete') {             
            steps {
                sh """
                #!/bin/bash
                sleep 60
                """
                }
                }
        
                stage('changing the previlige to root')
                steps{
                    sh """
                sudo su
                """
                }
    }
    stage('Moing the file towebapps to apache server'){
          steps
          {
              sh """
                cd /opt/apache-tomcat-10.1.34/webapps
                ls
                curl -L -u "Sample_creds_USR:Sample_creds_PWD" -O "http://3.94.159.27:8082/artifactory/hello-world-war-libs-release/com/efsavage/hello-world-war/1.0.28/hello-world-war-1.0.28.war"
                pwd
                
                """ 

            }
        }
         
    }
}
