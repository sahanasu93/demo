def choice=[]
node {
    choice = params["my-checkbox"].split(",")
}
pipeline {
  agent any
  parameters{
    string(name: 'PERSON', defaultValue: 'Vikas', description: 'Is he happy?')
    "CheckboxParameter": [(name:'my-checkbox', format: 'JSON', description: 'select any 1')
    {
      "key": "stage 1",
      "value": "stage 1"
    },
    {
      "key": "stage 2",
      "value": "stage 2"
    },
    {
      "key": "stage 3",
      "value": "stage 3"
    }
    {
      "key": "stage 4",
      "value": "stage 4"
    }
 ]
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
