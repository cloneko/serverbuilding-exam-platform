# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "dummy"
  config.vm.box_url = "https://github.com/mitchellh/vagrant-aws/raw/master/dummy.box"
  config.aws_extras.record_zone = "cloneko.com."
  config.aws_extras.record_name = ENV['LOGNAME'] + ".cloneko.com."
  config.aws_extras.record_type = "CNAME"
  config.aws_extras.record_ttl = "60"


  config.vm.provider :aws do |aws, override|
    aws.access_key_id    = ENV['AWS_ACCESS_KEY']
    aws.secret_access_key = ENV['AWS_SECRET_KEY']
    aws.keypair_name = "serverbuild2014"
    override.ssh.username = "ubuntu"
    override.ssh.private_key_path = "~/.vagrantssh/id_rsa"
    aws.instance_type = "t1.micro"
    aws.region = "us-west-1"
    aws.ami = "ami-ee4f77ab" # Default Ubunutu 14.04 LTS of US-WEST-1
    aws.security_groups = ['all']
    aws.tags = {
	'Name'=> ENV['LOGNAME']
    }
  end
end
