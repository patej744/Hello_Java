pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo 'building app'
            }
        }
    }

    stages {
        stage('test') {
            steps {
                echo 'testing app'
            }
        }
    }

    stages {
        stage('deploy') {
            steps {
                echo 'deploying app'
            }
        }
    }
}

node {
    // groovy script
}