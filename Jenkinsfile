podTemplate(containers: [
    containerTemplate(
        name: 'ansible', 
        image: 'benjfranklin/jenkins-agent-ansible:1.1',
        command: 'sleep', 
        args: '5m',
        runAsUser: 'ansible'
        )
  ]) {

    node(POD_LABEL) {
        stage('Testing Ansible Agent') {
            container('ansible') {
                stage('Shell Execution') {
                    sh '''
                    export PATH="/home/ansible/.local/bin:$PATH"
                    ansible --version
                    '''
                }
            }
        }

    }
}
