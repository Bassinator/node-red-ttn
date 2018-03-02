Vagrant.configure("2") do |config|

  config.vm.provider "docker" do |d|
    d.image = "bassualdo/centosvagrant"
    d.has_ssh = true
    d.ports = ["127.0.0.1:1880:1880"]
  end


  config.vm.provision "ansible_local" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "nodered.yml"
    ansible.install = true
  end
end
