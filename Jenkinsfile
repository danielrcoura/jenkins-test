pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                echo '-0-0-0-0-0-0-0- rodou esta linha! -0-0-0-0-0-0-0-'
            }
        }
        stage('test') {
          wget -O- -nv https://raw.githubusercontent.com/golangci/golangci-lint/master/install.sh | sh -s v1.35.2
          sh 'golangci-lint run -v --timeout 5m --disable-all --exclude-use-default=false --max-same-issues=0 --max-issues-per-linter=0 --enable gosec --out-format json > lint.json'
        }
    }
}