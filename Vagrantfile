Vagrant.configure("2") do |config|
  config.ssh.insert_key = true
  
  # Configurer Syslogsrv
  config.vm.define "Syslogsrv" do |syslog|
    syslog.vm.box = "ubuntu/focal64"
    syslog.vm.hostname = "Syslogsrv"
    syslog.vm.network "private_network", ip: "192.168.56.10"
  end

  # Configurer Linux01
  config.vm.define "Linux01" do |linux|
    linux.vm.box = "ubuntu/jammy64"
    linux.vm.hostname = "Linux01"
    linux.vm.network "private_network", ip: "192.168.56.11"
  end

  # Configurer Host02
  config.vm.define "Host02" do |kali|
    kali.vm.box = "kalilinux/rolling"
    kali.vm.hostname = "Host02"
    kali.vm.network "private_network", ip: "192.168.56.12"
  end
end

