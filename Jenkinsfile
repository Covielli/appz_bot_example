pipeline(
environment {dockerImage = ''}
agent any

stages{
stage ('Prepare'){
steps{
sh 'docker stop $(docker ps -q --filter "ancestor-labllbotcarrier")'
sh 'docker rm -f $(docker ps -q --filter "ancestor-labllbotcarrier" --filter "status-exited")
}
}
stage('Build'){
steps{
sh 'docker build -t lab11botcarrier /var/jenkins_home/workspace/DockerPipeline/Dockerfile'
}
}
stage('Deploy'){
steps{
sh 'docker run -d lab11botcarrier'
}
}
}
}
