pipeline {
    agent any
    tools {
        maven "maven-3.8.6"
        jdk "jdk19"
    }
    stages {
        stage('Initialize'){
            steps{
                echo "PATH = ${M2_HOME}/bin:${PATH}"
                echo "M2_HOME = /opt/maven"
            }
        }
        stage('Build') {
            steps {
                
                sh 'mvn -B -DskipTests clean package'
                
            }
        }
     } 
}
