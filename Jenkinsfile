pipeline {
   agent any
   tools {
        go 'go-1.15.17'
    }
    stages {
        stage('build') {
            steps {
                echo '-0-0-0-0-0-0-0- rodou esta linha! -0-0-0-0-0-0-0-'
            }
        }
        stage('test') {
          steps {
            sh 'curl -sfL https://install.goreleaser.com/github.com/golangci/golangci-lint.sh | bash -s -- -b ./bin v1.35.2'
            sh './issue-import'
          }
        }
    }
}