pipeline {
    agent {
        any {
            // image 'maven:3-alpine' 
            // args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                withMaven(maven : 'nonprod-maven')
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}