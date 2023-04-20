pipeline{
    agent any
    tools{maven 'M3'}
    stages{
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/Regliss/SpringPetClinic'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('Package'){
            steps{
                sh 'mvn package'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }
        stage('Deploy'){
            steps{
                sh 'java -jar /Users/cnm-tpo/.jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
            }
        }
    }
}
