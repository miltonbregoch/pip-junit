pipeline { 
    agent any 

	triggers {
        pollSCM('* * * * *')
    }
	 
	parameters{
		string(name: 'JAVA_HOME', defaultValue: 'C:/Program Files/Java/jdk-14', description: 'JDK', )
	}
	
    stages { 
        stage('STAGE 00'){ 
            steps{
                withAnt{
			  bat "C:\ant\bin\ant.bat -file build.xml test jar"
			}
            }
        }
    } 
} 
