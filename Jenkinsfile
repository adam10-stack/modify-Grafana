pipeline {
    agent any

    stages {
    
        stage('Change Title Tab Grafana') {
            steps {
                sh '''
                    find /usr/share/grafana/public/build/ -name '*.js' -exec sed -i 's#AppTitle="Grafana"#AppTitle="Izeno"#g' {} \;
                '''
            }
        }

        stage('Change Login Title') {
            steps {
                sh '''
                    find /usr/share/grafana/public/build/ -name '*.js' -exec sed -i 's#LoginTitle="Welcome to Grafana"#LoginTitle="Welcome to iZeno"#g' {} \;
                '''
            }
        }

    }
}

