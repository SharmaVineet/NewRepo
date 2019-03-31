pipeline
{
	agent any
	stages {
 		stage{
 			step("Code-Compile"){
 				echo "Performing Code Compile"
 				mvn compile
 			}
 			step("Code-Test"){
 				echo "Performing Code Testing"
 				mvn test
 			}
 			step("Code-Review"){
 				echo "Performing Code Review"
 				mvn pmd:pmd
 			}
 			step("Code-Metric"){
 				echo "Performing Code Metric"
 				mvn cobertura:cobertura -Dcobertura.report.format=xml
 			}
 			step("Code-Package"){
 				echo "Performing Code Packaging"
 				mvn package
 			}
 		}
 }
}
