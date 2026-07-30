pipeline {
    agent any

    tools {
        nodejs 'node24'
    }

    environment {
        SCANNER_HOME = tool 'sonar-scanner'
    }

    stages {

        stage('Git Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Wakekar/3_Tier_Application.git'
            }
        }

        stage('Install Package Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Unit Tests') {
            steps {
                sh 'npm test'
            }
        }

        stage('Trivy FS Scan') {
            steps {
                sh 'trivy fs --format table -o fs-report.html .'
            }
        }

        stage('SonarQube Analysis') {
            steps {
                withSonarQubeEnv('sonar') {
                    sh '''
                        $SCANNER_HOME/bin/sonar-scanner \
                        -Dsonar.projectKey=Campground \
                        -Dsonar.projectName=Campground
                    '''
                }
            }
        }

        stage('Docker Build & Tag') {
            steps {
                script {
                    withDockerRegistry(
                        credentialsId: 'docker-cred',
                        toolName: 'docker'
                    ) {
                        sh 'docker build -t aniketwakekar/camp:latest .'
                    }
                }
            }
        }

        stage('Trivy Image Scan') {
            steps {
                sh 'trivy image --format table -o image-report.html aniketwakekar/camp:latest'
            }
        }

        stage('Docker Push Image') {
            steps {
                script {
                    withDockerRegistry(
                        credentialsId: 'docker-cred',
                        toolName: 'docker'
                    ) {
                        sh 'docker push aniketwakekar/camp:latest'
                    }
                }
            }
        }
    }
}
