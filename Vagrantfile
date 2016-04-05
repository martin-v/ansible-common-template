Vagrant.configure(2) do |config|
	config.vm.box = "martin-v/debian-jessie-libvirt"
	config.vm.network :private_network, ip: "192.168.121.65"
	config.ssh.insert_key = false
	config.vm.define "common-debian" do |host|
		host.vm.provider :libvirt do |domain|
			domain.nested = true
			domain.volume_cache = 'none'
		end
		host.vm.provision :ansible do |ansible|
			ansible.verbose = "v"
			ansible.playbook = "playbook.yml"
			ansible.inventory_path = "staging.hosts"
		end
	end
end
