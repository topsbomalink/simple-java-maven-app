pipeline {
//     agent {
//             docker {
//                 image 'maven:3-alpine'
//                 args '-v /root/.m2:/root/.m2'
//             }
//         }
    agent { label 'jenkins_agent'}
    tools {
      maven '3.8.7'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('docker') {
            steps {
                script{
                    app = docker.build("simple-java-maven-app")
                }
            }
        }
    }
    
}
