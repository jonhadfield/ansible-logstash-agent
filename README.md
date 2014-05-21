logstash-agent
========

Ansible role which installs and configures a logstash-agent.

Requirements
------------

Tested on Anbsible 1.6

Role Variables
--------------


    logstash_agent_online_install: true                         # Whether or not to perform an online installation by downloading the installer
    logstash_agent_installer_path: /tmp/logstash-1.4.1.tar.gz   # Where to find the installer for an offline installation 
    logstash_agent_version: 1.4.1                               # The version of logstash to install
    logstash_agent_base_install_dir: /apps                      # Where logstash will be installed
    logstash_agent_base_logs_dir: /logs                         # Where logstash will log to
    logstash_agent_base_data_dir: /data                         # Where logstash will store its data
    logstash_agent_redis_hosts:                                 # Which redis servers to ship to
        - redis1
        - redis2
    logstash_agent_java_home:                                   # Specify java rather than try to detect
    logstash_agent_user: root                                   # User that owns the files and the process will run as
    logstash_agent_group: root                                  # Group ownership for the files
    logstash_agent_patterns_dir: /tmp/custompatterns/           # Custom patterns to copy (Use trailing slash to copy directory and not contents)
    logstash_agent_input_config: /tmp/input.conf                # Input and filter configuration



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
