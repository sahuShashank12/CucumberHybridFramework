pipeline 
{
    agent any
    
    tools
    { 
        maven 'MAVEN_HOME'
    }
    
    stages 
    {
        stage('Test') 
        {
            steps 
            {
                sh 'mvn clean test'
            }
        }

        stage('Report') 
        {
            steps 
            {
                echo 'Reports will be Generated and Published in Some time'
            }
        }
    }

    post
    {
        always
        {
            publishHTML (target: [
                allowMissing: false,
                alwaysLinkToLastBuild: false,
                keepAll: true,
                reportDir: 'test-output/SparkReport',
                reportFiles: 'Spark.html',
                reportName: "Functional Testing Results"
    	}

    }
}
