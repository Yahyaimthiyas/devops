
pipeline {

    agent any



    stages {



        stage('Clone') {

            steps {

                echo "Cloning repo..."

            }

        }



        stage('Build Docker Image') {

            steps {

                sh 'docker build -t my-jenkins-site .'

            }

        }



        stage('Deploy Container') {

            steps {

                sh 'docker stop mysite || true'

                sh 'docker rm mysite || true'

                sh 'docker run -d -p 8085:80 --name mysite my-jenkins-site'

            }

        }



    }

}


