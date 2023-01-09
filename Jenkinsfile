pipeline {
//     agent {
//         docker {
//             image 'maven:3.8.7-eclipse-temurin-11'
//             args '-v /root/.m2:/root/.m2'
//         }
//     }
    agent { label 'jenkins_agent' }
    stages {
        stage('Build') {
            steps {
                sh 'source /etc/profile'
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}