pipeline {
    agent any
    environment {
        registry = "mjordalopez/modeling-java"
    }

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage('Unit Test') {
            steps {
                 sh "mvn -Dtest=HelloControllerTest test"
            }
            post {
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                }
            }
        }


    }
}
