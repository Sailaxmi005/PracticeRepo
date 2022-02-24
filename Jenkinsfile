Pipeline{
  agent any
  stages {
        stage("Execute Master Branch") {
            when {
                branch 'master'
                  }
            steps {
                script {
                    git 'https://github.com/bsk1072/java-hello-world-with-maven-1.git'
                  echo "Jenkins File Read from Master"
                }
            }
        }
       stage("Execute developer Branch") {
            when {
                branch 'developer'
                  }
            steps {
                script {
                    git 'https://github.com/bsk1072/java-hello-world-with-maven-1.git'
                  echo "Jenkins File Read from Developer"
                }
            }
        }
      stage("Execute sailaxmi Branch") {
            when {
                branch 'sailaxmi'
                  }
            steps {
                script {
                    git 'https://github.com/bsk1072/java-hello-world-with-maven-1.git'
                  echo "Jenkins File Read from Sailaxmi"
                }
            }
        }
      stage("Execute Testing Branch") {
            when {
                branch 'testing'
                  }
            steps {
                script {
                    git 'https://github.com/bsk1072/java-hello-world-with-maven-1.git'
                  echo "Jenkins File Read form testing"
                }
            }
        }
  }
}
