Vagrant.configure("2") do |config|

  config.vm.define "psql" do |psql|
    psql.vm.box = "postgres"
    psql.vm.hostname = "postgres"
    psql.vm.network "public_network", use_dhcp_assigned_default_route: true, ip: "192.168.1.150"

    psql.vm.provider "virtualbox" do |v|
      v.gui = false
      v.name = "postgres"
      v.memory = 2048
      v.cpus = 2
    end
  end

  config.vm.define "web" do |web|
    web.vm.box = "postgres"
    web.vm.hostname = "web"
    web.vm.network "public_network", use_dhcp_assigned_default_route: true, ip: "192.168.1.200"

    web.vm.provider "virtualbox" do |v|
      v.gui = false
      v.name = "web"
      v.memory = 8192
      v.cpus = 4
    end
  end

end