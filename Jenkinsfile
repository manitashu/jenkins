pipeline {

//     agent {
//         //node { label 'workstation'}
//         //label 'JAVA'
//         none
//     }

    agent any

    stages {

        stage('Master Node') {
            agent {
                label 'MASTER'
            }
            steps {
                sh 'echo Hello'
            }
        }

        stage('Agent Node') {
            agent {
                label 'JAVA'
            }
            steps {
                sh 'echo Hi'
            }
        }
    }

    post {

        agent any

        always {
        //print 'Post Steps'
        sh 'echo Post Steps'
        }

    }
}