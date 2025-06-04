pipeline {
    agent any

    stages {
    
        stage('Change Title Tab Grafana') {
            steps {
                sh '''
                    sudo find /usr/share/grafana/public/build/ -name '*.js' -exec sed -i 's#AppTitle="Izeno"#AppTitle="Grafana"#g' {} ';'
                '''
            }
        }

        stage('Change Login Title') {
            steps {
                sh '''
                    sudo find /usr/share/grafana/public/build/ -name '*.js' -exec sed -i 's#LoginTitle="Welcome to iZeno"#LoginTitle="Welcome to Grafana"#g' {} ';'
                '''
            }
        }

    }
}
