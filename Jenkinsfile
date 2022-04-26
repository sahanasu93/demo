pipeline {
  agent any
  parameters{
    string(name: 'PERSON', defaultValue: 'Vikas', description: 'Is he happy?')
    booleanParam(description: 'select any 1', name: 'printperson')
    choice(choices: ['Stage 1', 'Stage 2', 'Stage 3', 'Stage 4'], description: 'select any', name: 'Build')
}
  stages {
    stage('Label 1') {
      when {branch 'master'}
      steps {
        script{
          if ("${params.printperson}" == 'true')
          {
        echo "${params.printperson}"
        echo "${params.PERSON}"
        echo 'test success'
        echo 'build' 
          }
        }
      }
    }
    stage('Label 2'){
      when {expression{params.Build == 'Stage 2' || params.Build == 'Stage 3' || params.Build == 'Stage 4'}
      branch 'feature'}
      steps{
        echo "Build number is ${currentBuild.number}"
        echo "His name is ${params.PERSON}"
      }
    }
    stage('Label 3'){
      when {expression{(params.Build == 'Stage 3' || params.Build == 'Stage 4' || params.Build == 'Stage 4') && env.BRANCH_NAME == 'feature'}}
      steps{
        echo "${params.PERSON} is from bangalore"
      }
    }
    stage('Label 4'){
      when { expression{params.Build == 'Stage 4'} }
      steps{
        echo "${params.PERSON} is married to sahana"
      }
    }
  }
}
