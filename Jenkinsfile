CODE_CHANGES = getGitChanges()

pipeline {
    agent any
    parameters {
        choice(name: 'version', choices: ['1.1','1.2','1.3'], description: '')
        booleanParam(name: 'executeTest', defaultValue: true, description: '')
    }
    stages {
        stage('build') {
            steps {
                echo 'building app'
            }
        }
        stage('test') {
            when {
                expression {
                    params.executeTest
                }
            }
            steps {
                echo 'testing app'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying app'
                echo "delpoying version ${params.version}"
            }
        }
    }
}