# Vagrant ansible deploy web server 

### Before you begin
1. You will need to install vagrant 
	1. on mac just  run `brew cask install virtual box`  and  `brew cask install vagrant` 
	2. on windows you will need to do extra steps [link](https://www.vagrantup.com/docs/installation/)
2. Install AWS plugin to vagrant `vagrant plugin install vagrant-aws`

## Version 
1. Vagrant 2.2.6
2. Ansible 2.8.5


## Before you run vagrant up 
1. clone the `git clone https://github.com/fsadykov/vagrant-projects.git` 
2. Run `cd web-server`
3.  You will need  to set up some environments 
	1. run `export AWS_ACCESS_KEY='Access key'`
	2. run `export AWS_SECRET_KEY='Secret key'`
4. After you set up everything run `vagrant up --provider=aws`
