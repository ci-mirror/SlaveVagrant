node('Windows-Server-2012-R2') {
    dir(currentBuild.id) {
        git changelog: false, poll: false, url: 'http://172.16.65.44/conanos/jenkins/slavevagrant'
        bat label: 'vagrant', script: '''vagrant up
        vagrant powershell --command build.bat
        vagrant destroy --force'''
    }
}