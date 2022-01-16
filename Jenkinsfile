pipeline {
    agent {
        docker {
            image 'maven:3.8.4-openjdk-11'
           
        }
    }
    stages {
        stage('git') {
            steps {
                git url: "https://github.com/Covielli/appz_bot_example.git"
            }
        }
        stage('Build') { 
            steps {
                sh 'mvn clean install'
                sh 'mvn -e exec:java -Dexec.mainClass="kpi.acts.appz.bot.hellobot.HelloWorldBot"'
            }
        }
    }
}
