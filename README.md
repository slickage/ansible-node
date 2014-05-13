# Ansible Node

Work in progress...

#### Configuration

1. Change the app name and deploy directory in `vars/defaults.yml`
2. Rename `hosts.example` to `hosts` and change it to your hosts. For Homebrew's
   ansible, this defaults to `/usr/local/etc/ansible/hosts`

#### Testing

`ansible all -i hosts -m ping -u vagrant --private-key=~/.vagrant.d/insecure_private_key`

#### Running

If you're using vagrant to create the box, please use the insecure SSH key `--private-key=~/.vagrant.d/insecure_private_key` in the `ansible-playbook` command.

    $ ansible-playbook -i hosts node-app.yml -t deploy
    $ <deploy your app>

[vbox]:    https://www.virtualbox.org/wiki/Downloads
[vagrant]: http://downloads.vagrantup.com/
[vbguest]: https://github.com/dotless-de/vagrant-vbguest
[hosts]:   https://github.com/cogitatio/vagrant-hostsupdater
