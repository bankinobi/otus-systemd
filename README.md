# otus-systemd

В Vagrantfile создается VM, provision step запускает на виртуальной машине Ansible playbook, выполняющий все три части ДЗ.

Для проверку выполнить команду **Vagrant up**

Внутри виртуальной машины выполнить команды:

    systemctl list-timers
    grep Master /var/log/messages
    systemctl status spawn-fcgi
    systemctl status httpd*
