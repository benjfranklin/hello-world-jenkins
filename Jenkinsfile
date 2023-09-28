podTemplate(containers: [
    containerTemplate(
        name: 'ansible', 
        image: 'ubuntu:latest'
        )
  ]) {

    node(POD_LABEL) {
        stage('Testing Ansible') {
            container('ansible') {
                stage('Shell Execution') {
                    sh '''
                    echo "hello world"
                    '''
                }
            }
        }

    }
}
