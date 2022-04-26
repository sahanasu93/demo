pipeline {
  agent any
  parameters{
    string(name: 'PERSON', defaultValue: 'Vikas', description: 'Is he happy?')
    booleanParam(description: 'select any 1', name: 'TOGGLE')
    choice(choices: ['Stage 1', 'Stage 2', 'Stage 3', 'Stage 4'], description: 'select any', name: 'Types of build')
}
  stages {
    stage('Stage 1') {
      when { expression { Stage 1 || Stage 2  } }
      steps {
        echo "${params.TOGGLE}"
        echo "${params.PERSON}"
        echo 'test success'
        echo 'build'
        echo 'completed'  
      }
    }
    stage('Stage 2'){
      steps{
        echo "${params.TOGGLE}"
        echo "His name is ${params.PERSON}"
      }
    }
    stage('Stage 3'){
      steps{
        echo "${params.TOGGLE}"
        echo "${params.PERSON} is from bangalore"
      }
    }
    stage('Stage 4'){
      steps{
        echo "${params.TOGGLE}"
        echo "${params.PERSON} is married to sahana"
      }
    }
  }
}
