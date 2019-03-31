pipeline {
agent any
stages {
   stage('Code-Compile') {
    steps {
     echo "Performing Code Compile"
     sh 'mvn clean install'
    }
   }	
   stage('Code-Test') {	
    steps {
     echo "Performing Code Testing"
     //mvn test
    }
   }
   stage('Code-Review') {	
    steps {
     echo "Performing Code Review"
     //mvn pmd:pmd
    }
   }
   stage('Code-Metric') {	
    steps {
     echo "Performing Code Metric"
     //mvn cobertura:cobertura
    }
   }
   stage('Code-Package') {	
    steps {
     echo "Performing Code Packaging"
     //mvn package
    }
   }	
  }
}
