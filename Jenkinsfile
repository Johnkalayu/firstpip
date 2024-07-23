pipeline {
    agent any
    tools{
        jdk {openjdk}
        mevan {m3}
    }
    stages {
        stage{
            step(SCM)
            scrept{
                ()
            }
        }
        stage{
            step("MAVEN BUILD")
            sh 'mvn clean install'

        }
        stage {
            step('DOCKER BUILD')
            sh 'docker build -t meme .'

        }
        stage {
            step('TESTING STAGES')
            sh ' mvn clean test'
            
        }