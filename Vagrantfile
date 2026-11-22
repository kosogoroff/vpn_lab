BOX_NAME = ENV['VAGRANT_BOX'] || 'bento/ubuntu-22.04'

Vagrant.configure("2") do |config|
  config.vm.box = BOX_NAME

  # Хук: срабатывает непосредственно перед запуском каждого провизионера,
  # в том числе при первом vagrant up
  config.trigger.before :provisioner_run, type: :hook do |trigger|
    trigger.info = "Генерируем inventory..."
    trigger.run = { path: "./generate_inventory.sh" }
    trigger.on_error = :halt   # упал скрипт — остановить vagrant, а не проскочить
  end

  config.vm.define "server" do |server|
    server.vm.hostname = "server.loc"
    server.vm.network "private_network", ip: "192.168.56.10"

    server.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/playbook.yml"
      ansible.inventory_path = "ansible/hosts"
      ansible.host_key_checking = false
      ansible.limit = "all"
    end
  end
end
