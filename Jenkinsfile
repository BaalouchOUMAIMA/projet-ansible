pipeline {
    agent any

    options {
        timestamps()
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Recuperation du projet depuis GitHub'
                checkout scm
            }
        }

        stage('Verification') {
            steps {
                echo 'Verification de la structure du projet'

                sh '''
                    pwd
                    ls -la

                    test -f inventory/inventory.ini
                    test -f playbooks/03-deploy-website.yml
                    test -f website/index.html

                    echo "Structure du projet valide"
                '''
            }
        }
    }
}