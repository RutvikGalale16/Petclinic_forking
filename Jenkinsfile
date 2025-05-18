pipeline{
    agent any
    tools {
        maven 'maven3'
        jdk 'jdk17'
    }
    stages{
        stage('Git Checkout'){
            steps{
                git branch: 'feature-2', url: 'https://github.com/RutvikGalale16/Petclinic_Rut'
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
                sh 'cp /home/jenkins/.jenkins/workspace/pipeline/target/petclinic.war /home/rutvik/30-days-of-devops/Day-4/jenkins_apache/apache-tomcat-9.0.65/webapps'
            }
        }
    }
}
