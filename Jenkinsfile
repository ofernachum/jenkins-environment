pipeline {
  agent any
  tools{
      jdk: 11
  }
  stages {
    stage('Compiling') {
      steps {
        echo "Compiling the code"
        sh 'javac Param.java'
      }
     }
    
    stage('Execute'){
      steps{
        echo "Execute the program with a parameter "
        sh 'java Param ${NAME}'
      }
    }
    stage('display the machine name'){
      steps{
        echo "And here I display the name of the machine "
        sh 'javac Maquina.java'
        sh 'java Maquina ${MACHINE}'
      }
    }
  }
}