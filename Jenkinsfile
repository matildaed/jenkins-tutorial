pipeline{
        agent any
        stages{
            stage('clone repo'){
                steps{
                    sh "git clone https://gitlab.com/qacdevops/chaperootodo_client "
                }
            }
                stage('deploy app '){
                steps{
                    sh "sudo docker-compose pull && sudo -E DB_PASSWORD=${DB_PASSWORD} docker-compose up -d"
                }
            }
        }
}
