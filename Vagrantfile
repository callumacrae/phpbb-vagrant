# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|
  config.vm.box = 'precise64'
  config.vm.hostname = 'phpbb-vagrant'

  config.vm.network :forwarded_port, guest: 8080, host: 8080
  config.vm.network :private_network, ip: '192.168.100.100'

  config.vm.synced_folder '.', '/vagrant',
                          mount_options: ["dmode=775,fmode=764"] # yolo

  config.vm.provider :virtualbox do |v|
    v.name = 'phpbb-vagrant'
  end

  config.vm.provision :ansible do |ansible|
    ansible.start_at_task = 'Make PHPUnit executable'
    ansible.playbook = 'playbook.yml'
  end
end
