pipeline {
  agent any
  tools {
    maven 'Maven'
  }
  stages {
    stage ('Initialize') {
      steps {
        sh '''
            echo "PATH = ${PATH}"
            echo "M2_HOME = ${M2_HOME}"
         '''
      }
    }
    stage ('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
  stage ('Deploy-To-Tomcat') {
            steps {
           sshagent(['tomcat']) {
                sh 'scp -o StrictHostKeyChecking=no target/*.war ec2-user@3.91.208.175:/home/ec2-user/prod/apache-tomcat-9.0.74/webapps/webapp.war'
              }      
           }       
    }
  }
}
