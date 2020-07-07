uclalib_role_zabbix [![Build Status](https://travis-ci.com/UCLALibrary/uclalib_role_zabbix.svg?branch=master)](https://travis-ci.com/UCLALibrary/uclalib_role_elasticsearch)
=========

This Zabbix role can be utilized to configure an agent AND/OR server setup. The current iteration only supports RHEL/CentOS 7.

Requirements
------------

This role was written with the intention of using other UCLA Library roles as dependencies. Please refer to the requirements.yml file to see what the dependencies are.

Available Tags
--------------

- server
- agent

Role Variables
--------------
By default, these variables are configured for a localhost setup. For a production workflow, you'll need to adjust the following variables pertinent to your environment.

Zabbix Agent(Mandatory)
#####
* `zabbix_agent_server`
* `zabbix_agent_service_active`

Zabbix Agent(Optional)
#####
* `zabbix_agent_listen_port`
* `zabbix_agent_hostname`
* `zabbix_agent_extra_config`

Zabbix Agent Log(Optional)
#####
* `zabbix_agent_log_type`
* `zabbix_agent_log_file`
* `zabbix_agent_log_file_size`
* `zabbix_agent_log_remote_commands`

Zabbix Server(Mandatory)
#####
* `zabbix_db_user_name`
* `zabbix_db_user_pw`
* `zabbix_db_name`
* `zabbix_db_host`
* `zabbix_db_port`

Zabbix Server(Optional)
#####
* `zabbix_trap_port`
* `zabbix_trap_timeout`
* `zabbix_pid_file_path`
* `zabbix_socket_dir`
* `zabbix_stats_allowed_ip`
* `zabbix_script_path_alerts`
* `zabbix_script_path_external`

Zabbix Server Log(Optional)
#####
* `zabbix_log_type`
* `zabbix_log_file`
* `zabbix_log_file_size`
* `zabbix_log_slow_queries_threshold`
* `zabbix_snmp_trap_log_file`

Dependencies
------------

Refer to requirements.yml file

Example Playbook
----------------

Refer to default/molecule/playbook.yml

License
-------

BSD

Author Information
------------------

- Anthony Vuong <avuong@library.ucla.edu>
- John Robinson <jhriv@library.ucla.edu>
