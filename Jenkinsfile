pipeline{
  agent any
  stages{
    stage('checkout'){
      step{
        echo 'Checking out repo'
        git 'https://github.com/sega270/new-repo.git'
      }
    }
    stage('Publish'){
      steps{
        publishHTML([
          allowMissing:true,
          alwaysLinkToLastBuild:false,
          keepAll:false,
          reportDir:'.',
          reportFiles:'new.html',
          reportName:'My HTML PIPE PAGE'
        ])  
      }
    }
  }
}
