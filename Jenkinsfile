pipeline {
    agent {
        label 'challenge'
    }
    environment {
        // The MY_KUBECONFIG environment variable will be assigned
        // the value of a temporary file.  For example:
        //   /home/user/.jenkins/workspace/cred_test@tmp/secretFiles/546a5cf3-9b56-4165-a0fd-19e2afe6b31f/kubeconfig.txt
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
