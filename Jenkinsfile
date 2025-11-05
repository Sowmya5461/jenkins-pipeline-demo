pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/username/project.git'Jenkinsfile

 pipeline {
  agent any
  stages {
    stage('Checkout') { steps { checkout scm } }
    stage('Build') {
      steps {
        sh 'echo Installing...'
        sh 'npm install'
      }
    }
    stage('Run') {
      steps {
        sh 'node server.js &'
        sh 'sleep 2'
        sh 'curl -f http://localhost:3000/health || echo Health check failed'
      }
    }
  }
  post {
    success { echo '✅ Build successful' }
    failure { echo '❌ Build failed' }
  }
}

            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'mvn clean package'   // Example for a Maven project
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
}
