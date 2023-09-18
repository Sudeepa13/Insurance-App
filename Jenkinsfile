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
       sh 'Build Package'
    }
  }

}

}

