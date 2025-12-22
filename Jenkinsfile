pipeline {
  // need to add agents
  agents any

  tools {
    // var 'mymaven': Jenkins tools configured under Global Tool Configuration
    // new tools added
    maven 'mymaven'
  }

  stages {

    stage('Clone Repo')
    {
      steps {
        git 'https://github.com/github-simplilearn-net.MavenBuild.git'
      }
    }

    stage('Compile Code')
    {
      steps {
        sh 'mvn compile'
      }
    }

    stage('Test Code')
    {
      steps {
        sh 'mvn test'
      }
    }

    stage('Package Code')
    {
      steps {
        sh 'mvn package'
      }
    }
    
  }
}
  
