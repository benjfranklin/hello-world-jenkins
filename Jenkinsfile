podTemplate(containers: [
    containerTemplate(
        name: 'ansible', 
        image: 'ansible/ansible'
        )
  ]) {

    node(POD_LABEL) {
        stage('Testing Ansible') {
            container('ansible') {
                stage('Shell Execution') {
                    sh '''
                    ansible --version
                    '''
                }
            }
        }

    }
}
