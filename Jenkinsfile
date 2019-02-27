node('Windows-Server-2012-R2') {
    echo 'Hello Vagrant...'
    echo currentBuild.id
    echo currentBuild.fullProjectName
    echo currentBuild.projectName
    env.fullProjectName = currentBuild.fullProjectName
    bat label: 'new_folder', script: '''md %fullProjectName%
    cd %fullProjectName%
    vagrant init opentable/win-2012r2-standard-amd64-nocm
    vagrant up'''
}