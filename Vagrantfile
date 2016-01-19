# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.provider "docker" do |docker|
    docker.vagrant_vagrantfile = "host/Vagrantfile"
    docker.image = "drupal"
    docker.create_args = ['--volume="/srv/myprofile:/var/www/html/profiles/myprofile"']
    docker.ports = ['80:80']
    docker.name = 'drupal-container'
  end
end