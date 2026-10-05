node {
    stage('Preparation') {
        catchError(buildResult: 'SUCCESS') {
            sh 'docker stop todoapp'
            sh 'docker rm todoapp'
        }
    }
    stage('Build') {
        build 'todoapp'
    }
}