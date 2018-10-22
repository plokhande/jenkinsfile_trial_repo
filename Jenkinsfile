/**
 * The node MUST have the following tools already installed
 * - Ansible
 * - Inspec
 * - Packer
 */
spinnaker_service_name = ['clouddriver', 'deck', 'echo', 'fiat', 'front50', 'gate', 'igor', 'orca', 'rosco']

node('ecs-infra-tools') {
    checkout scm
      stage('packer_build') {
        spinnaker_service_name.each { item ->
          sh """
          echo ${item}
          """
        }
}
}

