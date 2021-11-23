pipeline {

    agent any
    
    pipelineTriggers([ 
        upstream( 
           threshold: hudson.model.Result.SUCCESS, 
           upstreamProjects: "/multibranch /" + env.BRANCH_NAME.replaceAll("/", "%2F") 
        )
    ])

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
