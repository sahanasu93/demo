pipeline {
  agent any
  parameters{
    string(name: 'PERSON', defaultValue: 'Vikas', description: 'Is he happy?')
    properties([parameters([booleanParam('Toggle')])])
}
  stages {
    stage('stage 1') {
      if(Toggle == "true")
      steps {
        echo "${params.PERSON}"
        echo 'test success'
        echo 'build'
        echo 'completed'  
      }
    }
    stage('stage 2'){
      if(Toggle == "true")
      steps{
        echo "His name is ${params.PERSON}"
      }
    }
    stage('stage 3'){
      if(Toggle == "true")
      steps{
        echo "${params.PERSON} is from bangalore"
      }
    }
    stage('stage 4'){
      if(Toggle == "true")
      steps{
        echo "${params.PERSON} is married to sahana"
      }
    }
  }
}