pipeline { 
    agent any 

	triggers {
        pollSCM('* * * * *')
    }
	
    stages { 
        stage('STAGE 00'){ 
            steps{
                withAnt{
			  bat "ant -file build.xml test jar"
			}
            }
        }
    } 
} 
