pipeline {
  // need to add agents
  agent any

  tools {
    // var 'mymaven': Jenkins tools configured under Global Tool Configuration
    // new tools added
    maven 'Maven Install'
  }

  stages {

    stage('Clone Repo')
    {
      steps {
        git 'https://github.com/github-simplilearn-net/MavenBuild.git'
      }
    }

    stage('Compile Code')
    {
      steps {
        sh 'mvn clean compile -Dmaven.compiler.source=8 -Dmaven.compiler.target=8'
      }
    }

    stage('Test Code')
    {
      steps {
        sh 'mvn clean test -Dmaven.compiler.source=8 -Dmaven.compiler.target=8'
      }
    }

    stage('Package Code')
    {
      steps {
        sh 'mvn package -Dmaven.compiler.source=8 -Dmaven.compiler.target=8'
      }
    }
    
  }
}
  
