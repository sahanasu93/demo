pipeline {
  agent any
  parameters{
    string(name: 'PERSON', defaultValue: 'Vikas', description: 'Is he happy?')
    choice(name: 'Types', choices: 'stage1\nstage2\nstage3\nstage4', description: 'select any 1')
}
  stages {
    stage('stage 1') {
      when {stage stage1}
      steps {
        echo "${params.Types}"
        echo "${params.PERSON}"
        echo 'test success'
        echo 'build'
        echo 'completed'  
      }
    }
    stage('stage 2'){
      when {stage stage2}
      steps{
        echo "${params.Types}"
        echo "His name is ${params.PERSON}"
      }
    }
    stage('stage 3'){
      when {stage stage3}
      steps{
        echo "${params.Types}"
        echo "${params.PERSON} is from bangalore"
      }
    }
    stage('stage 4'){
      when {stage stage4}
      steps{
        echo "${params.Types}"
        echo "${params.PERSON} is married to sahana"
      }
    }
  }
}