pipeline {
  agent any
  environment {
     NOMBRE = "alberto"
     MAQUINA = """${sh(
           returnStdout: true,
           script: 'uname -n'
          )
          }"""
  }
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
    stage('compilarParam') {
      steps {
        echo "Estoy compilando el codigo de Param"
        sh 'javac Param.java'
      }
     }
    stage('ejecutarParam'){
      steps{
        echo "Y aquí  ejecuto PARAM "
        sh 'java Param ${NOMBRE}'
      }
    }
    stage('nombreMaquina'){
      steps{
        echo "Y aquí visualizeo el nombre de la maquina "
        sh 'javac Maquina.java'
        sh 'java Maquina ${MAQUINA}'
      }
    }
  }
}
