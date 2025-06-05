pipeline {
    agent any

    stages {
    
        stage('Change Grafana Tab Title') {
            steps {
                sh '''
                    sudo find /usr/share/grafana/public/build/ -name '*.js' -exec sed -i 's#AppTitle="Grafana"#AppTitle="iZeno"#g' {} ';'
                '''
            }
        }

        stage('Change Grafana Login Page Text') {
            steps {
                sh '''
                    sudo find /usr/share/grafana/public/build/ -name '*.js' -exec sed -i 's#LoginTitle="Welcome to Grafana"#LoginTitle="Welcome to iZeno"#g' {} ';'
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
