pipeline {
agent any
 tools {
    maven 'LocalMaven'
    jdk 'Local JDK'
  }
stages {
   stage('Code-Compile') {
    steps {
     echo "Performing Code Compile"
     sh 'mvn compile'
    }
   }	
   stage('Code-Test') {	
    steps {
     echo "Performing Code Testing"
     sh 'mvn test'
    }
   }
   stage('Code-Review') {	
    steps {
     echo "Performing Code Review"
     sh 'mvn pmd:pmd'
    }
   }
   stage('Code-Metric') {	
    steps {
     echo "Performing Code Metric"
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
