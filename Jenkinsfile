pipeline{
  agent any
  stages{
    stage('git-clone - Sithabile'){
        steps{
            checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-id', url: 'https://github.com/Team3-G4-Techops/Techops-Parallel-Job.git']]])
        }
    }
     stage('parallel-job 1'){
      parallel{
        stage('sub-job1 - Roger'){
          steps{
            sh 'sudo systemctl status jenkins'
			      sh 'ps -ef'
          }
        }
          stage('sub-job2 - Kingue'){
           steps{
            sh 'ps -ef'
    	      sh 'sudo systemctl status jenkins'
          }
        }
      }
    }
    stage('parallel-job 2'){
      parallel{
        stage('sub-job1 - Constance'){
          steps{
            sh 'ps -ef'
            sh 'sudo systemctl status jenkins'
          }
        }
      }
    }
  }
}
