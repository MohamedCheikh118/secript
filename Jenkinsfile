pipeline {
    agent {
        kubernetes {
            yaml '''
apiVersion: v1
kind: Pod
spec:
  containers:
  - name: python
    image: python:3.11
    command:
      - cat
    tty: true
'''
        }
    }

    stages {
        stage('Exécuter Python') {
            steps {
                container('python') {
                    sh 'python3 script.py'
                }
            }
        }
    }
}
