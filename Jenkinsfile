node
{
    def mavenHome = tool name: "maven3.8.4"
    
    stage('CheckoutCode')
    {
    git branch: 'development', credentialsId: 'ff525a3b-4062-4b7c-8115-f2bc5767d634', url: 'https://github.com/OSamaDevOps/maven-web-application.git'    
    }
    
    stage('Build')
    {
        sh "${mavenHome}/bin/mvn clean package"
    }
    /*
    stage('ExecuteSonarQube')
    {
        sh "${mavenHome}/bin/mvn clean sonar:sonar"
    }
    stage('UploadArtifactIntoNexus')
    {
        sh "${mavenHome}/bin/mvn clean deploy" 
    }
    stage('DeployAppIntoTomcat')
    {
      sshagent(['d5de1d1a-c225-450a-92ab-bdbd35fdfe51']) {
    sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@15.206.125.116:/opt/apache-tomcat-9.0.56/webapps/"
}  
    }
   stage('SendNotifications'){
   emailext body: '''Build Over...

Regards,
Osama Eqbal
7809099483''', subject: 'Build Over..', to: 'osama.devops4u@gmail.com'
}
*/
}
