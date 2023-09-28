podTemplate(containers: [
    containerTemplate(
        name: 'ansible', 
        image: 'benjfranklin/jenkins-agent-ansible:1.1',
        command: 'sleep', 
        args: '5m'
        )
  ]) {

    node(POD_LABEL) {
        stage('Testing Ansible Agent') {
            container('ansible') {
                stage('Shell Execution') {
                    sh '''
                        whoami
                        echo $PATH
                        ansible --version
                    '''
                }
            }
        }

    }
}
