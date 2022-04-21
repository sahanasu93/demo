def choice=[]
node {
    choice = params["my-checkbox"].split(",")
}
pipeline {
  agent any
  parameters{
    string(name: 'PERSON', defaultValue: 'Vikas', description: 'Is he happy?')
    CheckboxParameter(name:'my-checkbox', description: 'select any 1')
    {
      "key": "key-1",
      "value": "value-1"
    },
    {
      "key": "key-2",
      "value": "value-2"
    },
    {
      "key": "key-3",
      "value": "value-3"
    }
    {
      "key": "key-3",
      "value": "value-3"
    }
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
