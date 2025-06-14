pipeline{
    agent any
    tools {
        maven 'maven3'
        jdk 'jdk17'
    }
    stages{
        stage('Git Checkout'){
            steps{
                git branch: 'feature-2', url: 'https://github.com/RutvikGalale16/Petclinic_Rut.git'
            }
        }
        stage('compile'){
            steps{
                sh 'mvn clean compile'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn clean package'
            }
        }
        stage('Deployment'){
            steps{
                sh 'cp /home/rutvik/.jenkins/workspace/pipeline/target/petclinic.war /home/rutvik/Devops-Shack/30-Days-Of-Devops/Day-4/install_apache/apache-tomcat-9.0.65/webapps'
            }
        }
    }
}
