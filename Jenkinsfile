pipeline {
    agent {
    docker {
        image 'maven:3.8.1-openjdk-8'
        args '-v $home/.m2:/root/.m2'
        }
        }
    stages {
    stage('git') {
    steps {
    git url:"https://github.com/Covielli/bot_iit"
    }
    }
    stage('Build') {
    steps {
    sh 'mvn clean install'
    sh 'mvn -e exac:java -Dexec.mainClass="kpi.acts.appz.bot.hellobot.HelloWorldBot" -Dexec.args="5028762713:AAEXwTQ_K0jR-9H6OqgwdS7jmQhKs63Xm7s jenkinsiit_bot"'