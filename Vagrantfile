Vagrant::Config.run do |config|
	config.vm.box = "debian"
	config.vm.box_url = "http://mathie-vagrant-boxes.s3.amazonaws.com/debian_squeeze_32.box"
	config.vm.network :bridged
	config.vm.customize ["modifyvm", :id, "--memory", 512]
	config.vm.provision :puppet do |puppet|
		puppet.manifests_path = "manifests"
		puppet.manifest_file = "fortrabbit.pp"
		puppet.options = ["--templatedir", "/vagrant/templates"]
	end
end
