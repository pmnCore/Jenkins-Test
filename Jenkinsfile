pipeline {
    agent {docker { image 'python:latest'}}

    environment{
        COMMON_VARIABLE_FOR_STAGES = "horse ass"
        ANOTHER_COMMON_VARIABLE_FOR_STAGES = "amalgam"
    }

   stages {
      stage('Build stage') {
         steps {
            echo "Build number: $BUILD_NUMBER"
            sh "pwd"
            echo "Application has builded"
        }
      }
      stage('Test stage') {
         steps {
            echo "Executing some tests.."
            echo "Everything what we have is ${COMMON_VARIABLE_FOR_STAGES}"
            echo "But we have converted that into ${ANOTHER_COMMON_VARIABLE_FOR_STAGES}"
            echo "Test have been executed"
        }
      }
      stage('Deploy stage') {
         steps {
            echo "Deploying..."
            sh "python --version"
            echo "Application hasaa beeen deployed."
        }
      }
   }
}
