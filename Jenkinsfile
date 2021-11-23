pipeline {

    agent any
    
    options {
        pipelineTriggers([ 
            upstream( 
               threshold: hudson.model.Result.SUCCESS, 
               upstreamProjects: "/multibranch1/" + env.BRANCH_NAME.replaceAll("/", "%2F") 
            )
        ])
    }

    stages {
        stage(' Test') {
            steps {
                sh """
                echo "Running Unit Tests multibranch 2"
                """
            }
        }
    }   
}
