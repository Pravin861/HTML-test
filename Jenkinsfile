pipeline {
	agent any
	stages {
        stage('Checkout SCM') {
 		steps {
		git branch: 'main', credentialsId: 'Github', url: 'https://github.com/Pravin861/HTML-test.git'
		}
}
 	stage('Exeute shell') {
                steps {

                   sshPublisher(publishers: [sshPublisherDesc(configName: 'dev1', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'sudo sh /home/ubuntu/deploy.sh', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '/', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
                }
		}
            }
}