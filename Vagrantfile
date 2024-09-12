host_list = [
  {
    :name => "ansible1",
    :box => "bento/ubuntu-22.04"
  },
  {
    :name => "ansible2",
    :box => "bento/ubuntu-22.04"
  },
  {
    :name => "ansible3",
    :box => "bento/ubuntu-22.04"
  }
]

Vagrant.configure("2") do |config|
  host_list.each do |item|
    config.vm.define item[:name] do |host|
      host.vm.box = item[:box]
      host.vm.provider "vmware_desktop" do |vmware|
        vmware.gui = true
      end
    end
  end
end