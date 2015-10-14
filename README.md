WARNING: This role is no longer maintained !!!
==============================================

You are strongly encouraged to switch to the new roles stack on https://github.com/ElaoInfra
--------------------------------------------------------------------------------------------

By the way, this role will remain available on https://github.com/ElaoLegacy
----------------------------------------------------------------------------


Ansible Role - Symfony
=======================

A role to install symfony v1.X lib on your boxes !


Requirements
------------

This role will need PHP role providing by elao see https://galaxy.ansible.com/list#/roles/1275


Role Variables
--------------

    elao_php_symfony: # Array of symfony version
      -
        version:        1.4.20                      # Symfony version (Default will be last stable version: 1.4.20)
        install_path:   /usr/local/share/symfony    # Symfony local path (Default is /usr/local/share/symfony/{version_number})

Example Playbook
----------------

    - hosts: webservers
        vars:
            elao_php_symfony:
                - { version: 1.4.20, install_path: "/usr/local/share/symfony" }
                - { version: 1.0.22, install_path: "/usr/local/share/symfony" }
            roles:
                - { role: elao.php-symfony }


License
-------

MIT


Author Information
------------------

http://www.elao.com/
