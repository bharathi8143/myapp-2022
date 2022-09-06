@Library("bharathilibs") _
pipeline{
    agent any
    stages {
    stage("maven build"){
            steps{
                 sh 'mvn clean package -DskipTests=true'  
                 }
         stage("DevTomcat Deploy"){
            steps{
                tomcatdeploy("172.31.1.166","ec2-user","tomcat-dev")

                }
            }
        }
}
}
