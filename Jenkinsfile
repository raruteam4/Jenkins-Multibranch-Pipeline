pipeline { 
    agent any

    stages {
        stage('First') {
	    steps {
		script{
			env.EXECUTE="True"
		}
	    }
    }
	stage('Second') {
	    steps {
	    	when{
			equals ${EXECUTE}: "True"
		}
		script{
			sh 'echo "Updating Second Stage"'
		}
	    }
	} 
	stage('Third') {
	    steps {
		sh 'echo "Step Three"'
	    }
	}
    }
}
