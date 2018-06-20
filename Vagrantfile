Vagrant.configure("2") do |config|
  config.vm.box = "archlinux/archlinux"
  config.vm.hostname = "dev-env-arch"

  # Install Ansible
  config.vm.provision "shell",
    inline: "pacman --noconfirm -Sy ansible"

  # Provision with Ansible
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
