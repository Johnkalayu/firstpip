pipeline {
    agent any {
        tools (
            jdk (env.JAVA_HOME)
            maven (M3)

        )
    }
    stages{
        stage {
            step('SCM')
            sh 'https://github.com/Johnkalayu/firstpip.git'

        }
    }
    stages{
        stage {
            step('MAVEN CLEAN INSTALL')
            sh 'mvn clean install'

        }
    }
    stages{
        stage {
            step('DOCKER BUILD')
            sh 'docker build -t memmm .'

        }
    }
    stages{
        stage {
            step('MVN TEST')
            sh 'mvn clean test'
        }
    }
}

