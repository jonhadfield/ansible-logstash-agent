logstash-agent
========

Ansible role which installs and configures a logstash-agent.

Requirements
------------

Tested on Anbsible 1.6

Role Variables
--------------


    logstash_agent_online_install: true                     # Whether or not to perform an online installation by downloading the installer
    logstash_agent_installer_path: /var/installers          # Where to find the installer for an offline installation 
    logstash_agent_version: 1.4.0                           # The version of logstash to install
    logstash_agent_base_install_dir: /apps                  # Where logstash will be installed
    logstash_agent_base_logs_dir: /logs                     # Where logstash will log to
    logstash_agent_base_data_dir: /data                     # Where logstash will store its data
    logstash_agent_redis_hosts:                             # Which redis servers to ship to
        - redis1
        - redis2
        - redis3
    logstash_agent_java_home:                               # Specify java rather than try to detect


Dependencies
------------

None

Example Playbook
-------------------------

    - hosts: all
      sudo: yes
      roles:
         - logstash-agent

License
-------

MIT

Author Information
------------------

Jon Hadfield
