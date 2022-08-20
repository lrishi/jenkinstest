def buildSuccess = false
pipeline {
  agent any
  stages {
    stage("Generate Builds and Tests") {
      steps {
        echo "Came here"
      }
    }
    stage("Start Pipeline") {
      steps {
        script {
          def prl = [:]
          prl["Build"] = {
            stage("Build") {
              script {
                sleep 30
                buildSuccess = true
              }
            }
          }
          prl["Test 1"] = {
            stage("Test 1") {
                script {
                  waitUntil {
                    script {
                      return buildSuccess
                    }
                  }
                  sleep(2)
                }
            }
          }
          prl["Test 2"] = {
            stage("Test 2") {
                script {
                  waitUntil {
                    script {
                      return buildSuccess
                    }
                  }
                  sleep(3)
                }
            }
          }
          parallel prl
        }
      }
    }
  }  
}
