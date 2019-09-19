pipeline {
     agent any
     stages{
     stage('SCM') {
            steps {
                git url: 'https://github.com/MishraKD/assin11.git'
            }
        }
    stage('codeQuality & analysis') {
        steps {
                withSonarQubeEnv('sonarrunner2.4') {
                    // Optionally use a Maven environment you've configured already
                    withMaven(maven:'Maven 3.0.4') {
                        sh 'mvn clean package sonar:sonar'
                    }
                }
            }
    }
     
     }
}
