
node {

  stage('checkout sources') {
        // You should change this to be the appropriate thing
        git url:'https://github.com/vibhashah/specila-topics-lab6-ci.git'
  }

    stages {
        stage('build') {

        withMaven (maven: 'maven3') {
          sh "mvn package"
          echo "Hello World"
        }

        }

    }


}
