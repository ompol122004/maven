pipeline {
    agent any

    tools {
        maven "Maven3"
        jdk "Java21"
    }

    stages {
        stage('Initialize') {
            steps {
                echo "Pipeline Started"
            }
        }

        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }

    post {
        always {
            echo "Pipeline Finished"
        }
    }
}
