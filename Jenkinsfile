pipeline {
   agent any
   tools {
      maven 'M2_HOME'
         }
stages {
    stage('Git Checkout') {
  steps {
     git 'https://github.com/Sudeepa13/Insurance-App.git'
        }
    }
    stage('Build Package') {
    steps {
       sh 'mvn package'
    }
  }
    stage('Publish HTML Reports') {
       steps {
         publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, keepAll: false, reportDir: '/var/lib/jenkins/workspace/Insurance-Project/target/surefire-reports', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: '', useWrapperFileDirectly: true])
             }
         }
   /* stage('Create Docker image of App') {
       steps {
         sh 'docker build -t sudeedockeracc/insuranceapp:1.0 .'
             }
         }
     stage('Docker Image Push') {
       steps {
         withCredentials([usernamePassword(credentialsId: 'docid', passwordVariable: 'docpwd', usernameVariable: 'docusr')]) {
         sh 'docker login -u ${docusr} -p ${docpwd}'
       }
         sh 'docker push sudeedockeracc/insuranceapp:1.0'
   }    
     }   
    stage('Application Deploy-container') {
          steps {
            
           ansiblePlaybook credentialsId: 'ubuntu', disableHostKeyChecking: true, playbook: 'deploy.yml'
                }
          } */ 
    }
}



