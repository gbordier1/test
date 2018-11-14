def DEV_BRANCH_PATTERN = /^(develop|feature).*/
def RELEASE_BRANCH = 'master'

node("oinis"){
	try {
		stage ("Checkout scm"){
			cleanWs()
			checkout scm
		}
		stage ("Package"){
			echo "Create tar.gz"
			tar -zcvf test.tar.gz package2/*
		}
	}
	catch (Exception ex){
		emailext attachLog: true, subject: "Job '${JOB_NAME}' ($(BUILD_NUMBER)) is in " + currentBuild.result + " status"
		throw ex
	}
}
