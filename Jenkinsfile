pipeline {
    agent any

    stages {
        stage ('checkout source code from github') {

            steps {
                git credentialsId: 'git-credentials', url: 'https://github.com/dileep454/Helloworld1.git'
                }
            }
        
		stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_5_4') {
                    sh 'mvn clean install'
                }
            }
        }

        }
    }
}
