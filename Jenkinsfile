
node {
  stage('checkout sources') {
        // You should change this to be the appropriate thing
        git url: 'https://github.com/vibhashah/specila-topics-lab6-ci/tree/Vibha-ci'
  }

    stages {
        stage('Build') {

        withMaven (maven: 'maven3') {
          sh "mvn package"
          echo "Hello World"
        }

        }

    }

    post {
        always {
            archiveArtifacts artifacts: 'build/libs/**/*.jar', fingerprint: true
            junit 'target/surefire-reports/*.SampleJUnitTest/*.xml'
        }
    }


}