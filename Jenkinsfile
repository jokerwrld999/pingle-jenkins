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
        ENGINE_DIR = 'C:/Jenkins'
        folderPath = "${env.ENGINE_DIR}/Saved/UnrealBuildTool"
        srcPath = "${env.ENGINE_DIR}/Saved"
        destPath = "${env.ENGINE_DIR}/Archived.zip"
    }
    stages {
        stage ("Create Folder") {
            when {
                beforeAgent true
                    expression {
                        env.SKIP == "true"
                    }
            }
            steps {
                createFolder("${env.folderPath}")
            }
        }
        stage ("Remove Folder") {
            when {
                beforeAgent true
                    expression {
                        env.SKIP == "true"
                    }
            }
            steps {
                removeFolder("${env.folderPath}")
            }
        }
        stage ("Clean Folder") {
            when {
                beforeAgent true
                    expression {
                        env.SKIP == "true"
                    }
            }
            steps {
                cleanFolder("${env.folderPath}")
            }
        }
        stage ("Archive Folder") {
            // when {
            //     beforeAgent true
            //         expression {
            //             env.SKIP == "true"
            //         }
            // }
            steps {
                archiveFolder("${env.srcPath}","${env.destPath}")
            }
        }
    }
}