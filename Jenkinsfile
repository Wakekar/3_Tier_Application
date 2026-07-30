pipeline {
    agent any

    tools {
        nodejs 'node26'
    }

    environment {
        SCANNER_HOME = tool('sonar-scanner')
        IMAGE_NAME = 'aniketwakekar/camp:latest'
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

        stage('Trivy File System Scan') {
            steps {
                sh '''
                trivy fs \
                --format table \
                --output fs-report.html .
                '''
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

        stage('Docker Build') {
            steps {
                sh '''
                docker build -t ${IMAGE_NAME} .
                '''
            }
        }

        stage('Trivy Image Scan') {
            steps {
                sh '''
                trivy image \
                --format table \
                --output image-report.html \
                ${IMAGE_NAME}
                '''
            }
        }

        stage('Docker Login') {
            steps {
                withCredentials([
                    usernamePassword(
                        credentialsId: 'docker-cred',
                        usernameVariable: 'DOCKER_USERNAME',
                        passwordVariable: 'DOCKER_PASSWORD'
                    )
                ]) {
                    sh '''
                    echo "$DOCKER_PASSWORD" | docker login \
                    -u "$DOCKER_USERNAME" \
                    --password-stdin
                    '''
                }
            }
        }

        stage('Docker Push') {
            steps {
                sh '''
                docker push ${IMAGE_NAME}
                '''
            }
        }

        stage('Deploy To EKS') {
            steps {
                sh '''
                kubectl apply -f manifests/dss.yml
                '''
            }
        }

        stage('Verify Deployment') {
            steps {
                sh '''
                kubectl get pods -n webapps
                kubectl get svc -n webapps
                kubectl get deployment -n webapps
                '''
            }
        }

        stage('Docker Logout') {
            steps {
                sh 'docker logout'
            }
        }
    }

    post {

        always {
            archiveArtifacts artifacts: '*.html', allowEmptyArchive: true
        }

        success {
            echo '========================================='
            echo ' Pipeline Executed Successfully'
            echo ' Application Deployed to Amazon EKS'
            echo '========================================='
        }

        failure {
            echo '========================================='
            echo ' Pipeline Execution Failed'
            echo ' Please Check Jenkins Console Logs'
            echo '========================================='
        }

        cleanup {
            cleanWs()
        }
    }
}
