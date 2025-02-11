pipeline {
    agent any

    environment {
        JAVA_HOME = "/Library/Java/JavaVirtualMachines/jdk-17.jdk/Contents/Home"
        PATH = "${JAVA_HOME}/bin:/usr/bin:/bin:/usr/sbin:/sbin"
    }

    stages {
        stage('Initialize') {
            steps {
                script {
                    echo "Initializing Pipeline..."
                    sh 'java -version'
                }
            }
        }

        stage('Compile Java Code') {
            steps {
                script {
                    echo "Compiling Java program..."
                    sh 'javac TimestampPrinter.java'
                }
            }
        }

        stage('Run Java Program') {
            steps {
                script {
                    echo "Running Java program..."
                    sh 'java TimestampPrinter'
                }
            }
        }
    }

    post {
        always {
            echo "Cleaning up workspace..."
        }
    }
}
