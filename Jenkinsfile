/**
**/

library identifier: 'pingle-jsl@main', retriever: modernSCM(
  [$class: 'GitSCMSource',
   remote: 'https://github.com/jokerwrld999/pingle-jsl.git',
   credentialsId: 'github-creds'])

pipeline {
    agent {
      label 'win'
    }
    options {
        ansiColor('xterm')
    }
    // environment {
    // }
    stages {
        stage ("Build Image") {
            // when {
            //     anyOf {
            //         expression  {
            //             currentBuild.number == 1
            //         }
            //         changeset "src/**"
            //         changeset "Dockerfile"
            //     }
            // }
            steps {
                echo('Hello')
                sh('''
                  ls
                  pwd
                ''')
            }
        }
    }
}