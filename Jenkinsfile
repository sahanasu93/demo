pipeline {
  agent any
  parameters{
    string(name: 'PERSON', defaultValue: 'Vikas', description: 'Is he happy?')
    properties([parameters([extendedChoice(multiSelectDelimiter: ',', name: 'Type of stage', quoteValue: false, saveJSONParameterToFile: false, type: 'PT_CHECKBOX', value: 'Stage1,Stage2,Stage3,Stage4', visibleItemCount: 4)])])
}
  stages {
    stage('stage 1') {
      steps {
        echo "${params.PERSON}"
        echo 'test success'
        echo 'build'
        echo 'completed'  
      }
    }
    stage('stage 2'){
      steps{
        echo "His name is ${params.PERSON}"
      }
    }
    stage('stage 3'){
      steps{
        echo "${params.PERSON} is from bangalore"
      }
    }
    stage('stage 4'){
      steps{
        echo "${params.PERSON} is married to sahana"
      }
    }
  }
}
