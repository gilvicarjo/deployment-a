pipeline {
    agent {
        label 'challenge'
    }
    environment {
        
        MY_KUBECONFIG = credentials('config-jenkins')
    }
    stages {
        stage('Deploy Service A') {
            steps {
                sh("kubectl --kubeconfig $MY_KUBECONFIG apply -f deploymenta.yaml")
            }
        }
    }
}
