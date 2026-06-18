pipeline{
  agent any

  tools{
    gradle 'gradle'
    jdk 'jdk'
  }
  stages{
    stage("Checkout"){
      steps{
        git branch: 'main',
          url: "https://github.com/anjanm0545-dotcom/gdl5.git"
      }
    }
    stage("Build"){
      steps{
        sh 'gradle build'
      }
    }
    stage("test"){
      steps{
        sh 'gradle test'
      }
    }
    stage("Run Aplication"){
      steps{
        sh 'gradle run'
      }
    }
  }
  post{
    success{
      echo 'build and deploy sucessfull'
    }
    failure{
      echo 'build failed'
    }
  }
}

    
