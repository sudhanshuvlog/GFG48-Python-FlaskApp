pipeline { // pipeline - deployment-pipeline
    agent { label 'python-worker'} // agent where pipeline will be executed

    stages { // collection of jobs
        stage('Deploy the application') { // job 1
            steps { // the series of command , which will be executed in this job
               sh 'docker pull sudhanshuvlog/jinny1/gfg48-python-flaskapp:latest'
               sh 'docker run -dit --name webserver -p 80:80 gfg48-python-flaskapp '
            }
        }
        stage('Deployment Completed Message') { // job 2
            steps { // the series of command , which will be executed in this job
              echo "Deployment Completed Successfully"
            }
        }
    }
}
