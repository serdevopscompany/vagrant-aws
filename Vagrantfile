Vagrant.configure("2") do |config|
  config.vm.box = "dummy"

  config.vm.provider :aws do |aws, override|
    aws.access_key_id = ENV['AWS_KEY']
    aws.secret_access_key = ENV['AWS_SECRET']
    aws.keypair_name = ENV['AWS_KEYNAME']
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
