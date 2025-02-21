// pipeline {
//     agent any

//     stages {
//         stage('Build') {
//             steps {
//                 sh '''#!/bin/bash
//                 echo 'In C or Java, we can compile our program in this step'
//                 echo 'In Python, we can build our package here or skip this step'
//                 '''
//             }
//         }
//         stage('Test') {
//             steps {
//                 sh '''#!/bin/bash
//                 echo 'Test Step: We run testing tool like pytest here'

//                 # TODO fill out the path to conda here
//                 source /Users/xiangwang/anaconda3/bin/conda

//                 # TODO Complete the command to run pytest
//                 # sudo /PATH/TO/CONDA run -n <Envinronment Name> <Command you want to run>
//                 /Users/xiangwang/anaconda3/bin/conda run -n mlip pytest
//                 echo 'pytest runned'

//                 // echo 'pytest not runned'
//                 // exit 1 #comment this line after implementing Jenkinsfile
//                 '''

//             }
//         }
//         stage('Deploy') {
//             steps {
//                 echo 'In this step, we deploy our porject'
//                 echo 'Depending on the context, we may publish the project artifact or upload pickle files'
//             }
//         }
//     }
// }
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''#!/bin/bash
                echo 'Test Step: Running pytest'

                # Correctly initialize Conda
                source /Users/xiangwang/anaconda3/bin/activate
                
                # Run pytest inside Conda environment
                conda run -n mlip pytest

                echo 'pytest executed successfully'
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our project'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
