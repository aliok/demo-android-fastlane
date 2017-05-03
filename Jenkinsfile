node('android') {
    stage 'Checkout'
    checkout scm

    stage 'Build'
    sh "./gradlew clean assembleDebug --debug"

    stage 'Archive'
    archiveArtifacts artifacts: 'app/build/outputs/apk/*.apk', excludes: 'app/build/outputs/apk/*-unaligned.apk'
}
