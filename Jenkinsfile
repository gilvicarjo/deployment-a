pipeline {

  agent { label 'challenge' }

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