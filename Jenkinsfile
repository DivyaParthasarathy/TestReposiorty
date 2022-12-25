pipeline {
    agent any
    tools {
    maven 'maven-3.6.3' 
    }
    stages {
     stage ('Build') {
       steps {
         sh 'mvn clean package'
      }
    }

        
        stage ('Exec Maven') {
            steps {
                rtMavenRun (
                    tool: MAVEN_TOOL, // Tool name from Jenkins configuration
                    pom: 'pom.xml',
                    goals: 'clean install',
                    deployerId: "MAVEN_DEPLOYER",
                    resolverId: "MAVEN_RESOLVER"
                )
            }
        }

    }
}
