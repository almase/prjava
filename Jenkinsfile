pipeline {
  agent any
 
  stages {
    stage('compilar') {
      steps {
        echo "Estoy compilando el codigo"
        sh 'javac Simple.java'
      }
     }
    stage('ejecutar'){
      steps{
        echo "Y aquí lo ejecuto"
        sh 'java Simple'
      }
    }
  }
}
