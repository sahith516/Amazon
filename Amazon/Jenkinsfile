pipeline {
  agent any
 
  stages {
   
   stage('clone project') {
      steps {
           git branch:'master' , url:'https://github.com/sahith516/Amazon.git'
       }
   }
   
   stage('clean') {
       
      steps {
          dir ('Amazon'){
           sh 'mvn clean'
       }
   }
   }
   stage('compile') {
      steps {
                    dir ('Amazon'){

           sh 'mvn compile'
}
}
   }
 
   stage('test') {
      steps {
                    dir ('Amazon'){

           sh 'mvn test'
       }
        }
   }
   
 
   stage('build') {
      steps {
                    dir ('Amazon'){

           sh 'mvn clean install'
       }
      }
   }
  }
 
}
