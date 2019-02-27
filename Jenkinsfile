node('Windows-Server-2012-R2') {
    echo 'Hello Vagrant...'
    echo currentBuild.id
    echo currentBuild.fullProjectName
    echo currentBuild.projectName
    bat label: 'new_folder', script: 'md "${currentBuild.fullProjectName}${currentBuild.id}"'
}