Vagrant.configure("2") do |config|
  config.vm.box = "fedora/39-cloud-base"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbooks/default.yml"
    ansible.vault_password_file = ".vaultpw"
    ansible.extra_vars = "secrets.yml.enc"
  end
  config.vm.provider "libvirt" do |v|
    v.memory = 8192
    v.cpus = 4
  end
  config.ssh.insert_key = true
end
