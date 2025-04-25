pipeline {
    agent {
        docker {
            image 'python:3.11' // Image officielle qui contient déjà pip et Python
        }
    }

    stages {
        stage('Cloner le dépôt') {
            steps {
                echo "Le dépôt est déjà cloné par Jenkins automatiquement."
            }
        }

        stage('Tests Django') {
            steps {
                dir('Backend/odc') {
                    sh '''
                        pip install -r requirements.txt
                        python manage.py test
                    '''
                }
            }
        }

        stage('Docker Build') {
            steps {
                echo 'Construire l’image Docker ici...'
            }
        }

        stage('Lancement des services') {
            steps {
                echo 'Lancer les services ici...'
            }
        }
    }
}

