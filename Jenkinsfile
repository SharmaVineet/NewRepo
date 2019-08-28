pipeline {
agent any
stages {
   stage('Code-Compile') {
    steps {
     echo "Performing Code Compile Second Time"
     sh 'mvn compile'
    }
   }	
   stage('Code-Test') {	
    steps {
     echo "Performing Code Testing Second time"
     sh 'mvn test'
    }
   }
   stage('Code-Review') {	
    steps {
     echo "Performing Code Review Second Time"
     sh 'mvn pmd:pmd'
    }
   }
   stage('Code-Metric') {	
    steps {
     echo "Performing Code Metric First Time"
     sh 'mvn cobertura:cobertura'
    }
   }
   stage('Code-Package') {	
    steps {
     echo "Performing Code Packaging"
     sh 'mvn package'
    }
   }	
  }
}
