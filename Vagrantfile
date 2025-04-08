Vagrant.configure("2") do |config|
  config.vm.define "ubuntu" do |ubuntu|
    ubuntu.vm.box = "ubuntu/jammy64"
    ubuntu.vm.hostname = "ubuntu-test"

    config.vm.network "forwarded_port",
    guest: 8888, host: 8888, host_ip: "127.0.0.1"

    ubuntu.vm.provision "ansible" do |ansible|
      install_mode = :default
      ansible.playbook = "./ansible/playbooks/main.yml"
      ansible.extra_vars = {
      apache_http_port: 8888,
      apache_server_name: "prueba.localhost",
    }
    ansible.raw_arguments = ["-e", "ANSIBLE_CONFIG=/vagrant/ansible/ansible.cfg"]
    end
  end
end