pipeline{
    agent{
        label "worker1"
    }
    stages{
    // environment {
    //     AWS=credentials('aws_creds')
    // }
        stage("Init"){
            steps{
                withAWS(credentials: 'aws_creds', region: 'us-east-1'){
                    sh 'terraform -chdir=environments/dev init -upgrade'
                }
                  
                }
                
            post{
                always{
                    echo "be patient"
                }
                success{
                    echo " Initialized successfully"
                }
                failure{
                    echo "Init failed"
                }
            }
        }
        stage("Plan"){
            steps{
                 withAWS(credentials: 'aws_creds', region: 'us-east-1'){
                sh 'terraform -chdir=environments/dev plan'
                }
            }
            post{
                always{
                    echo "be patient"
                }
                success{
                    echo " plan executed successfully"
                }
                failure{
                    echo "Plan failed"
                }
            }
        }
        stage('Approval') {
            steps {
                script {
                    def userInput = input(id: 'confirm', message: 'Apply Terraform?', parameters: [ [$class: 'BooleanParameterDefinition', defaultValue: false, description: 'Apply terraform', name: 'confirm'] ])
                }
            }
        }
        stage("Apply"){
            steps{
                 withAWS(credentials: 'aws_creds', region: 'us-east-1'){
                sh 'terraform -chdir=environments/dev apply -auto-approve'
                }
            }
            post{
                always{
                    echo "be patient"
                }
                success{
                    echo " deployed successfully"
                }
                failure{
                    echo "deploy failed"
                }
            }
        }
         stage("kubeconfig"){
            steps{
                withAWS(credentials: 'aws_creds', region: 'us-east-1'){
                sh 'aws eks --region us-east-1 update-kubeconfig --name dev-eks'
                sh 'kubectl get pods --all-namespaces'
                }
            }
            post{
                always{
                    echo "be patient"
                }
                success{
                    echo " executed successfully"
                }
                failure{
                    echo "execution failed"
                }
            }
        }

    }
    post{
        always{
            echo "always"
        }
        success{
            echo "pipeline executed successfully "
        }
        failure{
            echo "pipeline execution failed"
        }
    }
}
    
    
    
    
    