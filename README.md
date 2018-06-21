# InfraCodeACI1

Infrastructure as Code template/example 1 for Cisco ACI and baremetal linux using Ansible and GitLab CI/CD

Consider these Ansible playbooks as a template/skeleton/sample that need customization for your particular environment and requirements.

## Prerequisites

- Working Cisco ACI fabric.
- Account granted an admin role.
- Baremetal linux host.
- Vault`ed passwords placed in host_vars/.
- Ansible configuraion somewere supposedly $HOME/.ansible.cfg.
- Ansible inventory somewere supposedly $HOME/.ansible.hosts with appropriate options and group definitions.
- Working GitLab installation with shell runner configured, tagged for ansible, registered, enabled/started and assinged to the project.
- Reflected ansible environment into gitlab-runner home directory (/var/lib/gitlab-runner/ in my case). Proper permissions must be set.

## Topology

Pretty trivial for the sake of cloning and reusing:

- Single APP of two EPGs.
- Single VRF per tenant.
- BD per EPG.
- Contract allowing communication b/w EPGs is common/default.

## Expected result:

![Sample result](doc/tst1_2018-06-20.png)
