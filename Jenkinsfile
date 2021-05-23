pipeline {
    agent any

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
                echo 'executing gradle...'
                withGradle {
                    sh '/var/lib/docker/volumes/jenkins_home/_data/plugins/gradle gradlew -v'                
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
