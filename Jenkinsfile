pipeline {
    agent {
        label 'generic'
    } //agent
    stages {
        stage("Setup script") {
            steps {
                sh """
                    sudo pip3 install pytest    
                 """
            } //steps
        } //stage
        stage("Run unit tests") {
            steps {
                sh """
                   sudo python -m pytest
                """    
            } //steps
        } //stage
    } //stages
    post {
        always {
            sh """
               sudo pip3 uninstall pytest -y
            """
        } //always
    } //post
} //pipeline
