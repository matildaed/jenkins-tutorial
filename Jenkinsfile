pipeline{
        agent any
        stages{
            stage('Make Directory'){
                steps{
                    sh "mkdir ~/chaperootodo_client"
                }
            }
           stage('clone repo'){
                steps{
                    sh "cd ~/chaperootodo_client"
                    sh "git clone https://gitlab.com/qacdevops/chaperootodo_client"
                }
            }
                stage('deploy app '){
                steps{
                    sh "cd ~/chaperootodo_client"
                    sh "sudo docker-compose pull && sudo -E DB_PASSWORD=${DB_PASSWORD} docker-compose up -d"
                }
            }
        }
}
