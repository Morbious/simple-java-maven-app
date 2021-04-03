pipeline {
    agent {
        docker {
            sh 'id'
            image 'maven:3-alpine' 
            args '-v $HOME/.m2:/root/.m2 --user root '
            sh 'id'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
