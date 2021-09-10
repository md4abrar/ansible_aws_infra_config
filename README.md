# ansible_aws_infra_config
Manage configurations in AWS infra using Ansible

Dynamic inventory can be managed using __ec2.py__ script and the configurations can be managed using __ec2.ini__

# cloudwatch_agent_installation 

1. aws_agent_installation.yml is the agent installation playbook
2. aws_cloudwatch_config.config has very basic cloudwatch agent loging metric this can be tweaked as per use case.

# ssm_agent_installation

1. ssm_agent_installation.yml is the playbook for installation  ssm agent

# Example : 

*List all hosts running in your AWS account*

###### ansible -i ./ec2.py all --list  

*Install AWS Cloud watch Agent on all listed ec2 instances*

###### ansible-playbook -i ./ec2.py aws_agent_installation.yml  
