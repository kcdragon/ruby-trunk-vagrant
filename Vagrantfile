# http://ruby-doc.org/core-2.1.0/doc/contributing_rdoc.html
# echo 'export PATH="/home/vagrant/.rubies/ruby-trunk/bin:$PATH"' >> ~/.bashrc
# source ~/.bashrc

# make && make install && make test && make test-all

# https://github.com/ruby/ruby/pull/813/commits/12a7ee672adbed9fdc1c71676cb9bbd44153b4d5

# /vagrant/test/rdoc/test_rdoc_rubygems_hook.rb: cannot load such file -- zlib
# /vagrant/test/webrick/test_ssl_server.rb: cannot load such file -- openssl
# extension library `fiddle' is not found
# extension library `zlib' is not found.  this may be false positive, but should assert because rubygems requires this
# extension library `openssl' is not found.  this may be false positive, but should assert because rubygems requires this

Vagrant.configure(2) do |config|

  config.vm.box = 'ubuntu/trusty64'

  config.vm.provider :virtualbox do |vb|
    vb.memory = '1024'
  end

  config.ssh.forward_agent = true

  config.vm.provision :shell, inline: <<-SHELL
if ! which autoconf
then
    apt-get -y install autoconf
fi

if ! which bison
then
    apt-get -y install bison
fi
SHELL

end
