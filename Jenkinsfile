pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v $HOME/.m2:/root/.m2 --user root '

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
