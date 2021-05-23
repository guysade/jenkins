pipeline {
    agent any
    
    tools {
        gradle 'Gradle-6.2'   
    }
    stages {
        stage('run frontend') {
            steps {
                echo 'executing yarn...'
                nodejs('Node-10.17') {
                    sh 'yarn install'
                }
            }
        }

        stage('run backend') {
            steps {
                echo 'executing gradle..'
                sh './gradlew -v'                
                }
            }
        }
        stage('test backend') {
            steps {
                echo 'checking gradle..'                
                }
            }
        }

        stage('build') {
            steps {
                echo 'building the app...'
            }
        }

        stage('test') {
            steps {
                echo 'testing the app...'
            }
        }

        stage('deploy') {
            steps {
                echo 'building the app...'
            }
        }
    }
}
