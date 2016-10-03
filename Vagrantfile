Vagrant.configure("2") do |config|
  config.vm.box = "dummy"

  config.vm.provider :aws do |aws, override|
    aws.access_key_id = "AKIAJQF4KMBMSZCNGULQ"
    aws.secret_access_key = "8JelsmMGJHrbWEO6WFhREU2mRcF/yjMOg8tj1TBl"
    aws.keypair_name = "sergio-key"
    aws.region = "us-east-1"
    aws.ami = "ami-d90d92ce"
    aws.instance_type = "t2.micro"
    aws.security_groups = "ssh-sgp"
    aws.tags = {
	'Name' => 'Provisioned by vagrant',
	}    

    override.vm.box = "dummy"
    override.ssh.username = "ubuntu"
    override.ssh.private_key_path = ENV['AWS_KEYPATH']
  end
end
