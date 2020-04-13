pipeline {
    agent {
        label 'generic'
    } //agent
    stages {
        stage("Setup script") {
            steps {
                sh """
                    pip3 install pytest    
                 """
            } //steps
        } //stage
        stage("Run unit tests") {
            steps {
                sh """
                   python -m pytest
                """    
            } //steps
        } //stage
    } //stages
    post {
        always {
            sh """
               pip3 uninstall pytest -y
            """
        } //always
    } //post
} //pipeline
