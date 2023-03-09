pipeline{
        agent any
        stages{
            stage('clone repo'){
                steps{
                    sh "git clone https://gitlab.com/qacdevops/chaperootodo_client ~/jenkins-tutorial-test/"
                }
            }
                stage('deploy app '){
                steps{
                    sh "sudo docker-compose pull && sudo -E DB_PASSWORD=${DB_PASSWORD} docker-compose up -d"
                }
            }
        }
}
