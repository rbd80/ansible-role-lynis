# ansible-role-lynis
=========
Ansible role to configure a enterprise lynis agent via shell 


## Assumptions
This repo is configured to use AWS System Store Parameter store and would be run within an ansible playbook.
```bash
AWS_PROFILE=packer_svc aws ssm put-parameter --name "lynis_key" --value "XXXXXXXXXXXXXX" --type String
```   



## Tigger
If any changes or updates you can force Ansible Galaxy to reload the role
```bash
sudo ansible-galaxy install --force -r terraform-aws-ami-secure/ansible/requirements.yaml
```

## Usage
This repo will create the pipeline and build two fresh AMIs for the environment.  This uses Ansible 
roles to configure logging, Systemd hardening, auditing and AntiVirus.  N  

## How to use
Make update the the env.rc file.  Setup the AWS configure with the account to create the IaaS
run the sh script to begin.

## AWS Accounts 
This repo relies on the "IaaS" accounts for AWS.  Follow the intructions this 
[repo](https://github.com/rbdgsa/aws-iaas-iam/) to configure the lowest level security 
 permissions for this repo.

## Help

**Got a question?**

File a GitHub [issue](https://github.com/rbd80/ansible-role-lynis/issues), send us an [email](mailto:robert.donovan@rxd.io).


## Contributing

### Bug Reports & Feature Requests

Please use the [issue tracker](https://github.com/rbd80/ansible-role-lynis/issues) to report any bugs or file feature requests.
