pipeline {
  agent any
  parameters{
    string(name: 'PERSON', defaultValue: 'Vikas', description: 'Is he happy?')
    booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
}
  stages {
    stage('stage 1') {
      steps {
        echo "${params.TOGGLE}"
        echo "${params.PERSON}"
        echo 'test success'
        echo 'build'
        echo 'completed'  
      }
    }
    stage('stage 2'){
      steps{
        echo "${params.TOGGLE}"
        echo "His name is ${params.PERSON}"
      }
    }
    stage('stage 3'){
      steps{
        echo "${params.TOGGLE}"
        echo "${params.PERSON} is from bangalore"
      }
    }
    stage('stage 4'){
      steps{
        echo "${params.TOGGLE}"
        echo "${params.PERSON} is married to sahana"
      }
    }
  }
}