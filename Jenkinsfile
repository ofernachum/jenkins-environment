pipeline {
  agent any
  environment {
     NAME = "Jenkins"
     MACHINE = "Linux"
     JAVA_OPTS="-Xms128m -Xmx512m"
  }
  stages {
    stage('Compiling') {
      environment{
        AUTHOR='Apasoft'
      }
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