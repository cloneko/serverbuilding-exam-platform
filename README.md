# Setup

## Global Setting

    aptitude install ruby ruby-dev gem make g++ rsync
    wget https://dl.bintray.com/mitchellh/vagrant/vagrant_1.6.3_x86_64.deb
    dpkg -i vagrant_1.6.3_x86_64.deb

## User Setting

    vagrant plugin install vagrant-aws
    vagrant plugin install vagrant-aws-extras
    git clone this repos
    
# Usage

    export AWS_ACCESS_KEY='YOUR_ACCESS_KEY'
    export AWS_SECRET_KEY='YOUR_SECRET_KEY'
    vagrant up

Login Server

    vagrant ssh

Destroy Server

    vagrant destroy
