node('Windows-Server-2012-R2') {
    echo 'Hello Vagrant...'
    echo currentBuild.id
    echo currentBuild.fullProjectName
    echo currentBuild.projectName
    withEnv(['build_folder=currentBuild.fullProjectName']) {
        bat label: 'new_folder', script: 'md %build_folder%'
    }
}