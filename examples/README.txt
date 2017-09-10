Basic instructions to run the examples in the book:

Download and install Vagrant.

Download and install Virtual Box.

In the  puppet-beginners-guide  repo directory, run:

  vagrant plugin install vagrant-vbguest
  vagrant up
   ...

  Machine booted and ready!


Connect to the VM with the following command:

vagrant ssh


You now have a command line shell on the VM. Check that Puppet is installed and working:

puppet --version

4.9.2


Try the 'Hello, world' example:

puppet apply /vagrant/examples/file_hello.pp
Notice: Compiled catalog for localhost in environment production in 0.07 seconds
Notice: /Stage[main]/Main/File[/tmp/hello.txt]/ensure: defined content as '{md5}22c3683b094136c3398391ae71b20f04'
Notice: Applied catalog in 0.01 seconds

cat /tmp/hello.txt
hello, world


To make sure you have the latest version of Puppet installed, run the following commands (answer  y  to any prompts):
 curl https://apt.puppetlabs.com/DEB-GPG-KEY-puppet |sudo apt-key add
 sudo apt-get update
 sudo apt-get install -y puppetlabs-release-pc1
 sudo apt-get install -y puppet-agent


To check that Puppet is installed and working, run this command (you may get a different version number, which is fine):
 sudo /opt/puppetlabs/bin/puppet --version
 4.10.0


Well, that was easy! Reward yourself with a big cup of tea and a slice of cake. It's important to keep your strength up.

You will get all the examples of the book in the examples folder of puppet-begginers-guide repo.
