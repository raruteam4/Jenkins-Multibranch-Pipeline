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
			expression{
				${EXECUTE}="True"
			}
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
