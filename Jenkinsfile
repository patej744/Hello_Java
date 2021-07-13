def gv 

pipeline {
    agent any
    parameters {
        choice(name: 'version', choices: ['1.1', '1.2', '1.3'], description: '')
        booleanParam(name: 'executeTest', defaultValue: true, description: '')
    }
    stages {
        stage('init'){
            steps{
                script{
                    gv = load "build.groovy"
                }
            }
        }
        stage('build') {
            steps {
                echo 'building app'
                script{
                    gv.buildApp()
                }
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
