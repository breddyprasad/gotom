pipeline {
 agent any 
  stages{
    stage('one'){
      steps{
          echo "Hi,this is prasad from devops Engineer"

}

}
     stage('two'){
       steps{
          input("Do you want to proced")

}
}

       stage('Three'){
        when {
         not{
                   branch "master"
         }
        }
        

         steps{
            echo "hello"
    }
    }
   
    
  stage('four') {

          parallel{
                stage('unit Test'){
                            steps{
                                echo "Running the unit test........"

                         }

}

stage('Integration test'){
                 agent{
                         docker{
                           reuseNode false
                            image 'ubuntu'
          }
}
 steps{
      echo "Running the integration testing....."

}
}
}
}
}
}
}


