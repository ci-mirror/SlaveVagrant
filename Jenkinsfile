node('Windows-Server-2012-R2') {
    env.BUILD_FOLDER=currentBuild.id
    bat label: 'vagrant', script: '''md %BUILD_FOLDER%
    cd %BUILD_FOLDER%
    vagrant init win-2012r2-standard-amd64-nocm-conan
    vagrant up'''
}