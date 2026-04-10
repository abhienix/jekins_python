pipeline {
	agent any 

	environement {
 	DOCKER_IMAGE ='hello-world-python:latest'

	}

	stages  { 
		stage ('Checkout'){



			git branch : 'main' , url:'https://github.com/abhienix/jekins_python.git>
	}

}


			stage ('Docker Build'){

			steps {
			script {

				if (FileExists('Dockerfile')){
					sh "docker build -t ${env.DOCKER_IMAGE}."
			} else {

				
		 error "Dockerfile not found in the workspace . Please create one for your python application."
}
}
}
}

			stage ('Docker Run (Optional)'){

			steps { 
				sh "docker run --rm ${env.DOCKER_IMAGE}"
			}
			}
			}
			
			Post {

			success {


			echo 'success'
			}	

			failure {
			echo 'failure'
}}}
