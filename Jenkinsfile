pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from version control (e.g., Git)
                // If you're using Git, uncomment the line below and add your repository URL
                // git url: 'https://github.com/your-repo/hello-world.git'
            }
        }

        stage('Build') {
            steps {
                // Compile the Java code
                sh 'javac src/main/java/org/example/Main.java'
            }
        }

        stage('Test') {
            steps {
                // Run tests (optional)
                // If you have tests, you can run them here using a testing framework like JUnit
                // Example: sh 'java -cp .:junit-4.12.jar:hamcrest-core-1.3.jar org.junit.runner.JUnitCore HelloWorldTest'
            }
        }

        stage('Run') {
            steps {
                // Execute the Java program
                sh 'java src/main/java/org/example/Main'
            }
        }
    }

    post {
        always {
            // Clean up workspace after the build
            cleanWs()
        }
    }
}
