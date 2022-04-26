pipeline {
  agent any
  parameters{
    string(name: 'PERSON', defaultValue: 'Vikas', description: 'Is he happy?')
    booleanParam(description: 'select any 1', name: 'printperson')
    choice(choices: ['Stage 1', 'Stage 2', 'Stage 3', 'Stage 4'], description: 'select any', name: 'Build')
}
  stages {
    stage('Label 1') {
      steps {
        echo "${params.printperson}"
        echo "${params.PERSON}"
        echo 'test success'
        echo 'build' 
      }
    }
    stage('Label 2'){
      when { expression{params.Build == 'Stage 2' || params.Build == 'Stage 3' || params.Build == 'Stage 4'} } && {$params.printperson == false}
      steps{
        echo "${params.printperson}"
        echo "His name is ${params.PERSON}"
      }
    }
    stage('Label 3'){
      when { expression{params.Build == 'Stage 3' || params.Build == 'Stage 4'} }
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
