pipeline {
    agent any  // ← ИСПОЛЬЗУЙТЕ ЛЮБОЙ ДОСТУПНЫЙ АГЕНТ
    
    stages {
        stage('Build') {
            steps {
                echo "🚀 Building application..."
                sh '''
                echo "Installing dependencies..."
                sleep 2
                '''
            }
        }
        
        stage('Test') {
            steps {
                echo "🧪 Running tests..."
                sh '''
                echo "Executing test suite..."
                sleep 2
                '''
            }
        }
        
        stage('Deliver') {
            steps {
                echo "📦 Delivering package..."
                sh '''
                echo "Preparing for delivery..."
                sleep 2
                '''
            }
        }
        
        stage('Deploy') {
            steps {
                echo "🚀 DEPLOYING TO PRODUCTION!"
                sh '''
                echo "Starting deployment process..."
                sleep 3
                echo "✅ Deployment completed successfully!"
                '''
            }
        }
    }
    
    post {
        always {
            echo "📊 Pipeline execution completed"
        }
        success {
            echo "🎉 All stages completed successfully!"
        }
        failure {
            echo "❌ Pipeline failed!"
        }
    }
}
