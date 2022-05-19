pipeline {
    agent none 
    stages {
        stage('SCM') {
            agent {label 'master' } 
            steps {
                git branch:'declarative', url: 'https://github.com/MattsManoj/spring-framework-petclinic.git'
            }
        }
        stage('Build') {
            agent { label 'build_java_11' } 
            steps {
                  sh 'mvn clean package'
            }
        }
    }
}
