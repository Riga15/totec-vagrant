#Totec Vagrant

Vagrantfile for Local Develop

## Installation

```bash
$ brew install caskroom/cask/brew-cask
```

```bash
$ brew cask install virtualbox
```

```bash
$ brew cask install vagrant
```

```bash
$ vagrant plugin install vagrant-vbguest
```

## Download Box Imange

```bash
$ vagrant box add centos6.7 https://github.com/CommanderK5/packer-centos-template/releases/download/0.6.7/vagrant-centos-6.7.box
```

## Start

```bash
$ vagrant up
```

```bash
$ vagrant provision
```

## Restart

```bash
$ vagrant reload
```

```bash
$ vagrant provision
```

## Stop

```bash
$ vagrant halt
```

## Destroy

```bash
$ vagrant Destroy
```
