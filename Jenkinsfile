node {
    stage('Preparation') {
        catchError(buildResult: 'SUCCESS') {
            sh 'docker stop samplerunning'
            sh 'docker rm samplerunning'
        }
    }
    stage('Build') {
        build 'SampleAppPipeline'
    }
    stage('Results') {
        build 'TestSampleApp'
    }
}
