podTemplate(containers: [
    containerTemplate(
        name: 'ansible', 
        image: 'benjfranklin/jenkins-agent-ansible:2.1.0',
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
                        which ansible-playbook
                    '''
                }
            }
        }

    }
}
