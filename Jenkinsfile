pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '5'))
    }
    tools {
        maven "maven-3.8.6"
        jdk "jdk19"
    }
    stages {
        stage('Build') {
            steps {
               withMaven(maven : 'maven-3.8.6') {
                   sh './test.sh'
               bat'mvn clean compile'
               }
            }
            }
        }
        //stage('Initialize'){
            //steps{
                //echo "PATH = ${M2_HOME}/bin:${PATH}"
                //echo "M2_HOME = /opt/maven"
            //}
        //}
        
                
}
