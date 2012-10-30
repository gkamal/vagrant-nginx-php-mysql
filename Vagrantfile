Vagrant::Config.run do |config|
  config.vm.box = "lucid32"
  config.vm.share_folder("v-root", "/vagrant", ".", :nfs => true)
  config.vm.network :hostonly, "33.33.33.33"
  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = ["cookbooks"]
    chef.add_recipe "apt"
    chef.add_recipe "build-essential"
    chef.add_recipe "php-fpm"
    chef.add_recipe "nginx"
    chef.add_recipe "php"
    chef.add_recipe "mysql"
    chef.add_recipe "git"
    chef.add_recipe "chef-phpunit"
  end
end
