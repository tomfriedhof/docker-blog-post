# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  
  config.vm.define "jenkins" do |v|
    v.vm.provider "docker" do |d|
      d.vagrant_vagrantfile = "./host/Vagrantfile"
      d.build_dir = "./Dockerfiles/jenkins"
      d.remains_running = true
      d.ports = ["8080:8080"]
      d.name = "jenkins-container"
    end
  end
  
  config.vm.define "drupal" do |v|
    config.vm.provider "docker" do |docker|
      docker.vagrant_vagrantfile = "host/Vagrantfile"
      # docker.image = "drupal"
      docker.build_dir = "."
      # docker.create_args = ['--volume="/srv/myprofile:/var/www/html/profiles/myprofile"']
      docker.ports = ['80:80']
      docker.name = 'drupal-container'
    end
  end
end