$mach_quant = 2

Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.cpus = 2
    vb.memory = "512"
    vb.check_guest_additions = false
  config.vm.box_check_update = false
  config.vm.box = "centos/7"
end

(1..$mach_quant).each do |i|
    config.vm.define "srv#{i}" do |srv|
      srv.vm.network "public_network", bridge: "en0"
      srv.vm.hostname = "srv#{i}"
    end
end

end
