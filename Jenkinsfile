node {
    stage 'Build Maven'
    git url: "git@github.com:imod/file-provider-test.git"
    wrap([$class: 'ConfigFileBuildWrapper', managedFiles: [[fileId: 'MVN_SETTINGS_1', targetLocation: '', variable: 'GLOBAL_SETTINGS']]]) {
        sh "echo {env.GLOBAL_SETTINGS}"
        sh "${tool 'mvn'}/bin/mvn clean install --settings '${env.GLOBAL_SETTINGS}'"
    }
}

