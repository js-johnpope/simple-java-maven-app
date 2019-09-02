pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                container('maven') {
                    sh 'mvn -B -DskipTests clean package'
                }
                // withMaven(maven : 'nonprod-maven')
                // sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}