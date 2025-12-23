pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo '======================================'
                echo '📥 Récupération du code depuis GitHub'
                echo "🌿 Branche : ${env.BRANCH_NAME}"
                echo "📦 Build : ${env.BUILD_NUMBER}"
                echo '======================================'
            }
        }
        
        stage('Vérification des fichiers') {
            steps {
                echo '======================================'
                echo '📂 Vérification des fichiers du projet...'
                echo '======================================'
                sh 'ls -la'
                sh 'pwd'
                echo '✅ Fichiers vérifiés!'
            }
        }
        
        stage('Build') {
            steps {
                echo '======================================'
                echo '🔨 Simulation de la compilation...'
                echo '======================================'
                sleep 2
                echo '✅ Build simulé avec succès!'
            }
        }
        
        stage('Test') {
            steps {
                echo '======================================'
                echo '🧪 Exécution des tests simulés...'
                echo '======================================'
                sleep 2
                echo '✅ Tests simulés avec succès!'
            }
        }
        
        stage('Deploy') {
            steps {
                echo '======================================'
                echo '🚀 Déploiement simulé...'
                echo '======================================'
                sleep 1
                echo '✅ Déploiement simulé avec succès!'
            }
        }
    }
    
    post {
        success {
            echo ''
            echo '✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅'
            echo '   PIPELINE RÉUSSI AVEC SUCCÈS!'
            echo "   Build #${env.BUILD_NUMBER}"
            echo '✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅'
            echo ''
        }
        failure {
            echo ''
            echo '❌ ❌ ❌ ❌ ❌ ❌ ❌ ❌ ❌ ❌'
            echo '   LE PIPELINE A ÉCHOUÉ!'
            echo '❌ ❌ ❌ ❌ ❌ ❌ ❌ ❌ ❌ ❌'
            echo ''
        }
        always {
            echo ''
            echo '🏁 Fin de l\'exécution du pipeline'
            echo "⏰ Build #${env.BUILD_NUMBER}"
            echo "🌿 Branche : ${env.BRANCH_NAME}"
            echo ''
        }
    }
}
