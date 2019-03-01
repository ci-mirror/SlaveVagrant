node('Windows-Server-2012-R2') {
    env.BUILD_FOLDER=currentBuild.id
    dir(currentBuild.id) {
        bat label: 'vagrant', script: '''vagrant box list'''
    }
}