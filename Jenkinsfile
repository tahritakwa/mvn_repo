pipeline {
stages {
    stage('Build') {
        agent { 
            docker {
                image 'maven:latest' 
                args '-v /root/.m2:/root/.m2' 
            }
        }
        steps {
            sh 'mvn -B -DskipTests clean package' 
        }
    }
    stage('Test') { 
        agent {
            docker {
                image 'maven:latest'
                args '-v /root/.m2:/root/.m2'
            }
        }
        steps {
            sh 'mvn test' 
        }
    }
    stage ('Build docker image') { 
        agent {
            docker {
                image 'maven:latest'
                args '-v /root/.m2:/root/.m2 -v /var/run/docker.sock:/var/run/docker.sock' 
            }
        }
        steps {
            sh 'mvn -Ddocker.skip=false -Ddocker.host=unix:///var/run/docker.sock docker:build' 
        }
    }
}
}
