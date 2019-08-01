  require 'vagrant-aws'
  Vagrant.configure("2") do |config|
  	config.vm.box = "dummy"
  	config.ssh.insert_key = false 
  	config.vm.provider 'aws' do |aws , override|
		override.nfs.functional = false
  		aws.access_key_id = "Your_access_key"
  		aws.secret_access_key = "Secret_access_key"
  		aws.keypair_name = 'Kaypair_name'
  		aws.instance_type = "t2.micro"
  		aws.region = 'ap-south-1'
  		aws.ami = 'ami-0d2692b6acea72ee6'
  		aws.security_groups = [ 'security_group_name' ]
  		override.ssh.username = 'ec2-user'
  		override.ssh.private_key_path = 'path_to_key'
		aws.elastic_ip = "your_generated_elastic_ip"
  	config.vm.provision "ansible" do |ansible|
  		ansible.verbose = 'v'
  		ansible.playbook = "playbook.yml"
		ansible.inventory_path = "inventory_path"
        end
     end
  end



