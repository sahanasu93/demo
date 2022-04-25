pipeline {
  agent any
  parameters{
    string(name: 'PERSON', defaultValue: 'Vikas', description: 'Is he happy?')
    booleanParam(description: 'select any 1', name: 'TOGGLE')
    choice(choices: ['Stage 1', 'Stage 2', 'Stage 3', 'Stage 4'], description: 'select any', name: 'Types of build')
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
