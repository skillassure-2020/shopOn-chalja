pipeline {
    agent any
    stages {
        stage('Build'){
            steps {
                echo "Build Project"
                sh label: '', script: 'mvn clean install'
            }
        }
        stage('JAVA RUN'){
            steps{
                echo "JAVA RUN"
                //sh label: '', script: 'javac ./src/test/java/com/ShopOn/TestRunner/TestRunner.java'
                //sh label: '', script: 'java ./src/test/java/com/ShopOn/TestRunner/TestRunner'
                sh label: '', script: '''ProjectPath=$WORKSPACE
classpath=$WORKSPACE\\target\\classes;$WORKSPACE\\target\\test-classes\\*
java com.ShopOn.TestRunner'''
            }
        }
    }
}
