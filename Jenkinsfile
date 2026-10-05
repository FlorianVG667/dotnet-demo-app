node {
    
    stage('Preparation') {
        catchError(buildResult: 'SUCCESS', stageResult: 'SUCCESS') {
            sh 'docker compose down -y || true'
        }
    }
    stage('Checkout') {
        checkout scm
    }
    stage('Build + deploy') {
        sh 'docker compose up -d --build'
    }
}