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
    environment {
        ENGINE_DIR = 'C:\\Jenkins'
        folderPath = "${env.ENGINE_DIR}\\Saved\\UnrealBuildTool"
    }
    stages {
        stage ("Create Folder") {
            steps {
                echo('Hello')
                createFolder("${env.folderPath}")
            }
        }
    }
}