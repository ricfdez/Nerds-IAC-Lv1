#Fundamentos de la virtualizacion

## Descargar Git para Windows
- Buscar su version: https://git-scm.com/download/win
- Instalar y probar comandos basicos de GIT
- `git clone` `git diff`
- Crearse una cuenta de github.com
- Bonus - acceder desde VSCode a Github y loguearse

## Descargar Virtual box
- En esta web: https://www.virtualbox.org/wiki/Downloads busquen su sistema operativo
- Instalar en su maquina, asegurarse de que la instalacion funciona

## Descargar Vagrant:
- https://developer.hashicorp.com/vagrant/install?product_intent=vagrant
- Buscar su sistema operativo
- Descargar e instalar la version que corresponda a su sistema operativo
- Bonus - buscar sobre infrastructura en codigo, que es Vagrant?

## Configurar maquina virtual: Ubuntu Desktop:
- Abrir powershell en su maquina Windows como admin. (click derecho, ejecutar como administrador)
- En la terminal ejecutamos estos comandos:
``` shell
cd ~ 
mkdir ubuntu-desktop
cd ubuntu-desktop
New-Item -ItemType File -path ./Vagrantfile
```

## Abrimos VSCODE
- Abrimos el directorio donde creamos el archivo `Vagrantfile`
- Abrimos con vscode el archivo `Vagrantfile` 
- Colocamos el siguiente codigo:
``` shell
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  
  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = "2048"
    vb.cpus = 2
  end

  config.vm.provision "shell", inline: <<-SHELL
    sudo apt update
    sudo apt install -y ubuntu-desktop
    sudo apt install -y virtualbox-guest-dkms virtualbox-guest-utils virtualbox-guest-x11
    sudo reboot
  SHELL
end
```
- Guarden el archivo, con `CTRL`+`S`

## Volvemos a Powershell, usamos el comando `Vagrant up`
- Que pasa con Virtualbox?
- Pueden usar el comando Vagrant up en otro folder?
