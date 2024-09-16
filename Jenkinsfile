pipeline {
  agent any
  environment {
     NAME = "Jenkins"
     MACHINE = "Linux"
  }
  stages {
    stage('Compiling') { 
      environment {
        AUTHOR='Apasoft'
        JAVA_OPTS="-Xms128m -Xmx512m"
      }  
      steps {
        echo "Compiling the code"
        sh 'javac Param.java'
        echo "The author is ${AUTHOR}"
      }
     }
    
    stage('Execute'){
      steps{
        echo "Execute the program with a parameter "
        sh "java Param ${NAME}"
      }
    }
    stage('display the machine name'){
      steps{
        echo "And here I display the name of the machine "
        sh 'javac Machine.java'
        sh "java Machine ${MACHINE}"
      }
    }
  }
}
