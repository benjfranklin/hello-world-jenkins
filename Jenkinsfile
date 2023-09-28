podTemplate(containers: [
    containerTemplate(
        name: 'ubuntu', 
        image: 'ubuntu:latest'
        )
  ]) {

    node(POD_LABEL) {
        stage('Testing Ubuntu') {
            container('ubuntu') {
                stage('Shell Execution') {
                    sh '''
                    echo "hello world"
                    '''
                }
            }
        }

    }
}
