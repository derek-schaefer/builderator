# vim: ft=ruby:

Vagrant.configure(2) do |config|
  config.vm.hostname = 'builderator'
  config.vm.box = 'ubuntu/xenial64'

  config.vm.provider :virtualbox do |virtualbox|
    virtualbox.name = 'builderator'
    virtualbox.cpus = 4
    virtualbox.memory = 2048
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = 'playbook.yml'
    ansible.verbose = true
  end
end
