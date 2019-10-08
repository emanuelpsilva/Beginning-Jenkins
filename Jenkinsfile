node {
    printMessage("Pipeline Start")

    stage("Fetch Source Code") {
        git "https://github.com/emanuelpsilva/Beginning-Jenkins"
    }

    dir('Lesson5/ActivityA') {
		
		stage("Install make"){
			sh 'apk add make'
		}
		
		stage("Install virtualenv"){
			sh 'apk add python-pip'
			sh 'pip3 install virtualenv'
		}
		
        stage("Install Requirements") {
            sh 'make install'
        }

        stage("Run Tests") {
            sh 'make jenkins_test'
        }

        stage("Deploy") {
            if (env.BRANCH_NAME == "master") {
                printMessage("deploying master branch")
            } else {
                printMessage("no deployment specified for this branch")
            }
        }
    }

    printMessage("Pipeline End")
}

def printMessage(message) {
    echo "${message}"
}
