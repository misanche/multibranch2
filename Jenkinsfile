pipeline {

    agent any
    
    /*triggers {
        upstream( 
           threshold: hudson.model.Result.SUCCESS, 
           upstreamProjects: "/multibranch1/" + env.BRANCH_NAME.replaceAll("/", "%2F") 
        )
    }*/

    stages {
        stage(' Test') {
            steps {
                echo "Param from multibranch1  ${params.VERSION_NUMBER}"
            }
        }
    }   
}
