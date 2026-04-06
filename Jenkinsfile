pipeline {
    agent any

    stages {
        stage('checkout'){
            steps{
                git branch: 'main', url:'https://github.com/sega270/new-repo.git'
            }
        }

        stage('Publish'){
            steps{
                publishHTML([
                    //default parameters
                    allowMissing:true,
                    alwaysLinkToLastBuild:false,
                    keepAll:false,

                    //these parameters changes acc.
                    reportDir:'.',            // . is root directory
                    reportFiles:'demo.html',   // name of html file
                    reportName:'MY HTML PAGE'
                ])
            }
        }
    }
}

