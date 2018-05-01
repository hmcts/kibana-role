Role Name
=========

Installs and configures Kibana.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

* `kibana_pkg_version` - What RPM package version to install
* `kibana_server_host` - This setting specifies the host of the back end server.
* `kibana_server_name` - A human-readable display name that identifies this Kibana instance.
* `kibana_server_port` - Kibana is served by a back end server. This setting specifies the port to use.
* `kibana_server_default_route` - This setting specifies the default route when opening Kibana. You can use this setting to modify the landing page when opening Kibana.
* `kibana_elasticsearch_url` - The URL of the Elasticsearch instance to use for all your queries.


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: reform.kibana, kibana_elasticsearch_url: http://elasticsearch.host:9200 }
