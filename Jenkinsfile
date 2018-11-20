 pipeline {
    stages {
        stage('API Testing') {
            steps {
                sh '''rm -rf newman
newman run -r junit demo.postman_collection.json'''
            }
            post {
                always {
                    junit 'newman/*.xml' 
                }
            }
        }
        
    }
}