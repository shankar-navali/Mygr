pipeline{
	agent any
	
	tools{
	    gradle 'Gradle'
	    jdk 'JDK'
	    }
	stages{
	    stage('Checkout'){
		steps{
		   git branch: 'master', url:'https://github.com/shankar-navali/Mygr.git'
		   }
	     }
	     
	     stage('Build'){
		 steps{
		    sh 'gradle build'
		    }
	     }
	     
	     stage('Test'){
		steps{
		   sh 'gradle test'
		   }
		}
	     stage("Run Application'){
	     	steps{
	     	   sh 'gradle run'
	     	   }
	     }
	  }
 	 
 	 post{
 	 	success{
			echo 'Build successfully'
		}
		
		failure{
			echo 'Failed in build'
		}
	}
}
