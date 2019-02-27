node('Windows-Server-2012-R2') {
    echo 'Hello Vagrant...'
    echo currentBuild.id
    echo currentBuild.fullProjectName
    echo currentBuild.projectName
    def x =currentBuild.fullProjectName
    withEnv(['build_folder=${env.x}']) {
        bat label: 'new_folder', script: 'md %build_folder%'
    }
}