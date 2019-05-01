
node {
  stage('checkout sources') {
        // You should change this to be the appropriate thing
        git url: 'https://github.com/vibhashah/specila-topics-lab6-ci/tree/Vibha-ci'
  }

    stages {
        stage('Build') {

        withMaven/ (maven: 'maven3') {
          sh "mvn package"
        }
            steps {
                sh './gradlew build'
                echo "Hello World!!!"
            }
        }
        stage('Test') {
            steps {
                sh './gradlew check'

            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'build/libs/**/*.jar', fingerprint: true
            junit 'build/reports/**/*.xml'
        }
    }


  //stage('Build') {
    // you should build this repo with a maven build step here
    //echo "hello"
  //}
  // you should add a test report here
}