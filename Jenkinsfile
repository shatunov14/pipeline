pipeline {
    agent { 
        node {
            label 'docker-agent-trial'
        }
    }
    
    stages {
        stage('Build') {
            steps {
                echo "🚀 Building application..."
                sh '''
                echo "Installing dependencies..."
                # Здесь могут быть ваши реальные команды сборки
                sleep 2
                '''
            }
        }
        
        stage('Test') {
            steps {
                echo "🧪 Running tests..."
                sh '''
                echo "Executing test suite..."
                # Тестовые команды
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
                echo "Step 1: Copying files..."
                echo "Step 2: Restarting services..."
                echo "Step 3: Verification..."
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
            emailext (
                subject: "Pipeline SUCCESS: ${currentBuild.fullDisplayName}",
                body: "The pipeline completed successfully!",
                to: "admin@example.com"
            )
        }
        failure {
            echo "❌ Pipeline failed!"
        }
    }
}
