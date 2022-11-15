// pipeline {
//     agent any
//     stages {
//         stage('node') {
//             agent{
//                 docker {image 'node:16.13.1-alpine'}
//             }
//             steps {
//                 sh 'node --version'
//             }
//         }
//         stage('python') {
//             agent{
//                 docker{image 'python'}
//             }
//             steps {
//                 sh 'python3 --version'
//             }
//         }
//     }
// }
pipeline{
    agent any
    stages{
        stage("Cleaning workspace")
        {
            steps{
                // Clean before build
                cleanWs()
            }
        }
        stage("Python"){
            agent{
                docker { image 'learningmw1991/my_print_exec:01' }
            }
            steps{
                sh 'docker run -it learningmw1991/my_print_exec:01'
            }
        }
        stage('node') {
            agent{
                docker { image 'node:16.13.1-alpine' }
            }
            steps {
                sh 'node --version'
            }
        }
    }
}