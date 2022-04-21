pipeline {
  agent any
  parameters{
    choice(name: 'choose',
      choices: 'one\ntwo\nthree\nfour',
      description: 'which stage should run?')
    string(name: 'PERSON', defaultValue: 'Vikas', description: 'Is he happy?')
  }
  stages {
    stage('stage 1') {
      steps {
        echo "${params.choose}"
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
