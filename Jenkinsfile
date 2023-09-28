podTemplate(containers: [
    containerTemplate(
        name: 'ubuntu', 
        image: 'ubuntu:latest',
        command: 'sleep', 
        args: '5m'
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
