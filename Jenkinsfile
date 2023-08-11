node('maven-17') {
    checkout scm
    timeout(time: 5, unit: 'MINUTES') {
        ansiColor('xterm') {
            withEnv(['MAVEN_OPTS=-Djansi.force=true']) {
                sh 'mvn -B -Dstyle.color=always -ntp clean verify'
            }
        }
    }
}
