@Library("bharathilibs") _
pipeline{
    agent any
    stages{
        stage("Maven Build"){
            when {
                branch "develop"
            }
            steps{
               sh "mvn package"
            }
        }
       stage("Deploy To dev"){
            when {
                branch "develop"
            }
            steps{
               echo "deploying to development server...."
            }
        }
        stage("Deploy To Test"){
            when {
                branch "qa"
            }
            steps{
               echo "deploying to test server...."
            }
        }
        stage("Deploy To production"){
            when {
                branch "master"
            }
            steps{
               echo "deploying to master server...."
            }
        }
    }
}
    stage("maven build"){
            steps{
                 sh 'mvn clean package -DskipTests=true'  
            }
                 }
         stage("DevTomcat Deploy"){
            steps{
                tomcatdeploy("172.31.1.166","ec2-user","tomcat-dev")

                }
            }
        }
}