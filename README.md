# Vagrant_aws
Install using standard Vagrant 1.1+ plugin installation methods. After installing, vagrant up and specify the aws provider. An example is shown below.

$ vagrant plugin install vagrant-aws
...
$ vagrant up --provider=aws
...
Install the dummy box for vagrant :
$ vagrant box add dummy https://github.com/mitchellh/vagrant-aws/raw/master/dummy.box

Get the access_key $ Secret_access_key from your aws account, follow the following steps
-> Go to My Security Credentials on the aws-console 
-> select access_key $ Secret_access_key and 
-> create new
Save the credentials and use then in the Vagrantfile(vagrantfile is auto-generated when we initiate vagrant)
-> go to the security groups section 
-> generate keypair(this is the key to mention for ssh)
-> generate elastic ip to be used 
-> Create aa security group and allow inbound$iutbound rules as per the requirements(make sure to allow ssh)

DEPENDENCIES:
if get an error for ruby install the compatible ruby version
download: https://www.ruby-lang.org/en/downloads/
