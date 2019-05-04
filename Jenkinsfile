
node {
try {
  stage('checkout sources') {
        // You should change this to be the appropriate thing
        git url:'https://github.com/vibhashah/specila-topics-lab6-ci.git'
  }
    stage('build') {

        withMaven (maven: 'maven3') {
          sh "mvn package"
          echo "Hello World"
        }

        }

    }
    catch {
       sh "Ex"
    }
    finally{

      junit 'target/surefile-reports/*.SampleJUnit.xml'
    }


}
