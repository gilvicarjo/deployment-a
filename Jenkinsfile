pipeline {

  agent { label '2021' }

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/gilvicarjo/deployment-a.git', branch:'master'
      }
    }

    stage('Deploy Service A') {
      steps {
        script {
          kubernetesDeploy(configs: "deploymenta.yaml", kubeconfigId: "5")
        }
      }
    }

  }

}