pipeline {
    agent any

    stages {
    
        stage('change tittle tab grafana') {
            steps {
                sh '''
                    find /usr/share/grafana/public/build/ -name '*.js' -exec sed -i 's#AppTitle="Grafana"#AppTitle="Izeno"#g' {} \;
                '''
            }
        }

        stage('change login tittle') {
            steps {
                sh '''
                    find /usr/share/grafana/public/build/ -name '*.js' -exec sed -i 's#LoginTitle="Welcome to Grafana"#LoginTitle="Welcome to iZeno"#g' {} \;
                '''
            }
        }
        
    }
}
