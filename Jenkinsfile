pipeline{
  agent any
  stages{
    stage('Checkout'){
      step{
        echo 'Checking out repo'
        git 'https://github.com/sega270/new-repo.git'
      }
    }
    stage('Publish'){
      steps{
        publishHTML([
          allowmissing:true,
          alwaysLinktoLastBuild:false,
          keepAll:false,
          reportDir:'.',
          reportFiles:'new.html',
          reportName:'My HTML PIPE PAGE'
        ])  
      }
    }
  }
}
