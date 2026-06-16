pipeline{
  agent any
  tools{
   maven 'Maven'
   }
  stages{
   stage('chekout'){
    steps{
     git branch:'master',url:'https://github.com/Disha-L12/rkd1.git'
     }
     }
    stage('build'){
    steps{
     sh 'mvn clean package'
     }
     }
   stage('test'){
   steps{
   sh 'mvn test'
   }
   }
   stage('run'){
   steps{
   sh 'java -jar target/rkd1-1.0-SNAPSHOT.jar'
   }
   }
   }
post{
  success{
  echo 'success'
  }
  failure{
  echo 'fail'
  }
  }
  }
