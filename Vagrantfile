Vagrant.configure("2") do |config|
  config.vm.box = "dummy"

  config.vm.provider :aws do |aws, override|
    aws.access_key_id     = ENV["AWS_ACCESS_KEY"]
    aws.secret_access_key = ENV["AWS_SECRET_KEY"]
    aws.keypair_name      = "vagrant-key"
    aws.region            = "us-east-1"
    aws.ami               = "ami-7747d01e"



    override.ssh.username = "ubuntu"
    override.ssh.private_key_path = "vagrant-key.pem"

    override.vm.synced_folder ".", "/vagrant", disabled: true
    vagrant_synced_folder_default_type = ""

    config.vm.provision "ansible" do |ansible|
      ansible.limit = "all"
      ansible.playbook = "web-server.yaml"
   end
  end
end
