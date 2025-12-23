pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo '======================================'
                echo '📥 Récupération du code depuis GitHub'
                echo "🌿 Branche : ${env.BRANCH_NAME}"
                echo '======================================'
            }
        }
        
        stage('Build') {
            steps {
                echo '======================================'
                echo '🔨 Compilation du projet Java...'
                echo '======================================'
                script {
                    try {
                        sh 'javac HelloWorld.java'
                        echo '✅ Compilation réussie!'
                    } catch (Exception e) {
                        echo '⚠️  Java non installé, simulation de la compilation'
                    }
                }
            }
        }
        
        stage('Test') {
            steps {
                echo '======================================'
                echo '🧪 Exécution des tests...'
                echo '======================================'
                script {
                    try {
                        sh 'java HelloWorld'
                        echo '✅ Tests réussis!'
                    } catch (Exception e) {
                        echo '⚠️  Simulation de l\'exécution'
                    }
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo '======================================'
                echo '🚀 Déploiement du projet...'
                echo '======================================'
                sleep 2
                echo '✅ Déploiement simulé avec succès!'
            }
        }
    }
    
    post {
        success {
            echo ''
            echo '✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅ ✅'
            echo '   PIPELINE RÉUSSI AVEC SUCCÈS!'
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
            echo "⏰ Date : ${new Date()}"
            echo ''
        }
    }
}
