Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-20.04"
  config.vm.define :vagrant do |vagrant|
  config.vm.hostname = "WP-01-DEV"
  config.vm.network "forwarded_port", guest: "80", host: "8080"''
  end

  config.vm.provider :virtualbox do |virtualbox|
    virtualbox.name = "WP-01-DEV"
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "allup.yml"
#    ansible.raw_arguments  = "--user=vagrant"
#    ansible.raw_arguments  = "--private-key=~/.vagrant.d/insecure_private_key"
#    ansible.raw_arguments  = "--ask-vault-pass"
#    ansible.galaxy_role_file = "requirements.yml"
  end
end
