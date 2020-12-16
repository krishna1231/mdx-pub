import groovy.json.JsonOutput

ALL_NAMESPACES = ['dev','qa']

pipeline {
    agent any
    parameters {

        string(name: 'Db_Name', defaultValue: 'Default-Redis_DB', description: 'Enter DB Name')
        choice(name: 'target_env', choices: ALL_NAMESPACES, description: 'choose an environment')
    }
    stages {
        stage('Example') {
            steps {
                echo "${params.Db_Name} created!"
                echo "${params.target_env} Env Selected"
                echo "this line will only appear in idwh-migration branch"
            }

        }
    }
}
