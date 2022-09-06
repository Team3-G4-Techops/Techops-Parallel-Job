pipeline{
  agent any
  stages{
    stage('git-clone'){
        steps{
            checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/Team3-G4-Techops/Techops-Parallel-Job.git']]])
        }
    }
  }
}