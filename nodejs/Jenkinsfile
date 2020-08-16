def PATH = '/home/mp_task/HelloWorld_MPtask/nodejs'
pipeline {
        agent any
        stages {
                stage ('checkout'){
                           checkout scm
                     }
                stage ('build'){
                steps {
                        sh """
                            cd $PATH
                            docker build -t Dockerfile .
                           """
                       }
                    }

                }
}
}
