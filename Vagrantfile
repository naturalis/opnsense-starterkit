Vagrant.configure("2") do |config|

  # firewall
  config.vm.define "firewall" do |config|
    config.vm.box_version = "1.2"
    config.vm.box = "rudibroekhuizen/opnsense"
    #config.vm.box = "build/packer_virtualbox-iso_virtualbox.box"
    config.vm.provider "virtualbox" do |vb|
      vb.name = "firewall"
      #nic1, vagrant
      #nic2, oob
      #nic3, wan
      #nic4, lan
      vb.customize ["modifyvm", :id, "--nic4", "intnet"]
      vb.customize ["modifyvm", :id, "--intnet4", "lan"]
    end
  end

  # workstation
  config.vm.define 'workstation' do |config|
    config.vm.box = "peru/ubuntu-18.04-desktop-amd64"
    config.vm.provider 'virtualbox' do |vb|
      vb.name = "workstation"
      vb.customize ['modifyvm', :id, "--nic1", "intnet"]
      vb.customize ['modifyvm', :id, '--intnet1', "lan"]
    end
  end
end


# vagrant box remove build/packer_virtualbox-iso_virtualbox.box
