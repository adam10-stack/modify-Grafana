pipeline {
    agent any

    stages {
    
        stage('Change Grafana Tab Title') {
            steps {
                sh '''
                    sudo find /usr/share/grafana/public/build/ -name '*.js' -exec sed -i 's#AppTitle="iZeno"#AppTitle="Grafana"#g' {} ';'
                '''
            }
        }

        stage('Change Grafana Login Page Text') {
            steps {
                sh '''
                    sudo find /usr/share/grafana/public/build/ -name '*.js' -exec sed -i 's#LoginTitle="Welcome to iZeno"#LoginTitle="Welcome to Grafana"#g' {} ';'
                '''
            }
        }
		
		stage('Test Grafana Connection') {
            steps {
                sh '''
                    wget http://grafana:3000
                '''
            }
        }
    }
}
