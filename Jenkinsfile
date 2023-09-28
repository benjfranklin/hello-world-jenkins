podTemplate(containers: [
    containerTemplate(
        name: 'ansible', 
        image: 'benjfranklin/jenkins-agent-ansible',
        command: 'sleep', 
        args: '5m'
        )
  ]) {

    node(POD_LABEL) {
        stage('Testing Ansible Agent') {
            container('ansible') {
                stage('Shell Execution') {
                    sh '''
                    echo "hello world\n"
                    ansible --version
                    '''
                }
            }
        }

    }
}
