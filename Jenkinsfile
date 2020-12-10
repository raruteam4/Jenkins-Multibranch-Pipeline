pipeline { 
    agent any

    stages {
        stage('First') {
	    steps {
		script{
			env.EXECUTE="True"
			sh 'echo "variable asignada"'
		}
	    }
    }
	stage('Second') {
	    when{
		expression{
		    EXECUTE="True"
		}
	    }
	    steps{
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
