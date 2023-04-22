0x0A. Configuration management

                              _
 _ __  _   _ _ __  _ __   ___| |_
| '_ \| | | | '_ \| '_ \ / _ \ __|
| |_) | |_| | |_) | |_) |  __/ |_
| .__/ \__,_| .__/| .__/ \___|\__|
|_|         |_|   |_|
Learning Objectives
General

Intro to Configuration Management
Puppet’s Declarative Language: Modeling Instead of Scripting
Puppet lint
Puppet emacs mode
Environment

OS: Ubuntu 20.04 LTS
Terminal: Bash 5.0.17
Puppet
Style guidelines: Puppet Style Guide
Puppet lint
Install puppet

$ apt-get install -y ruby=1:2.7+1 --allow-downgrades
$
$ apt-get install -y ruby-augeas
$
$ apt-get install -y ruby-shadow
$
$ apt-get install -y puppet
$
Install puppet-lint

$ gem install puppet-lint
$
execute scripts

# puppet-lint --version
puppet-lint 2.5.2
# puppet-lint 0-create_a_file.pp
#
# puppet apply 0-create_a_file.pp
Notice: Compiled catalog for 6712bef7a528.ec2.internal in environment production in 0.04 seconds
Notice: /Stage[main]/Main/File[school]/ensure: defined content as '{md5}f1b70c2a42a98d82224986a612400db9'
Notice: Finished catalog run in 0.03 seconds
#
# ls -l /tmp/school
-rwxr--r-- 1 www-data www-data 13 Mar 19 23:12 /tmp/school
# cat /tmp/school
I love Puppet
$
# puppet apply 1-install_a_package.pp
Notice: Compiled catalog for d391259bf577 in environment production in 0.14 seconds
Notice: Applied catalog in 0.20 seconds
# gem list

*** LOCAL GEMS ***

puppet-lint (2.5.0)
#
Terminal #0 - starting my process

# cat killmenow
#!/bin/bash
while [[ true ]]
do
    sleep 2
done

# ./killmenow
Terminal #1 - executing my manifest

# puppet apply 2-execute_a_command.pp
Notice: Compiled catalog for d391259bf577.hsd1.ca.comcast.net in environment production in 0.01 seconds
Notice: /Stage[main]/Main/Exec[killmenow]/returns: executed successfully
Notice: Finished catalog run in 0.10 seconds
#
Terminal #0 - process has been terminated

# ./killmenow
Terminated
#
Autor

ESERE CYNTHIA Roys77111
