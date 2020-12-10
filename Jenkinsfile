pipeline { 
    agent any

    stages {
        stage('First') {
	    steps {
		script{
			env.EXECUTE="False"
			sh 'echo "variable asignada como: " ${EXECUTE}'
		}
	    }
    }
	stage('Second') {
	    when{
		expression{
		    EXECUTE=="True"
		}
	    }
	    steps{
		script{
                   sh 'echo "Updating Second Stage"'
                }
	    }
	} 
	stage('Third') {
	    when{
	        expression{
		    EXECUTE=="True"
		}
	    }
	    steps {
		sh 'echo "Step Three"'
	    }
	}
    }
}
