pipeline {
    agent any
    stages {
        stage("Checkout") {
            steps {
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/main']],
                    userRemoteConfigs: [[
                        url: 'https://github.com/Kimjibeom/jenkins.git',
                        credentialsId: 'github-token',
                        refspec: '+refs/heads/*:refs/remotes/origin/*' 
                    ]]
                ])
            }
        }
    }
}

