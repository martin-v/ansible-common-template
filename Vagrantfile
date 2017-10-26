Vagrant.configure(2) do |config|
	config.vm.box = "debian/stretch64"
	config.vm.box_version = "9.1.0"
	config.vm.synced_folder ".", "/vagrant", disabled: true

	config.vm.provider :libvirt do |domain|
		domain.nested = true
		domain.volume_cache = 'none'
	end
	config.ssh.insert_key = false

	config.vm.define "common-debian65" do |host|
		host.vm.network :private_network, ip: "192.168.121.65"
	end

	config.vm.define "common-debian66" do |host|
		host.vm.network :private_network, ip: "192.168.121.66"
	end

	config.vm.provision :ansible do |ansible|
		ansible.verbose = "v"
		ansible.playbook = "playbook.yml"
		ansible.inventory_path = "staging.hosts"
	end

end
