pipeline{
  agent any
    stages {
    stage('One'){
      steps{
             echo 'Hi, this is Hemant Kumar Yaranagula'
        }
       }
     stage('Two'){
       steps{
              input('Do you want to Proceed?')
             }
            }
     stage('Three'){
       steps{
              echo 'Hello Branch is master'
          }
         }
     stage('Four'){
        parllel{
              stage('Unit test'){
                        steps{
                                echo 'Running Unit test'
                              }
                            }
               stage('Integration test'){
                        agent {
                            docker {
                                    reusenode false
                                    image 'ubuntu'
                                   }
                               }
                             }
                }
               }
            }
}
