Overview
========

This cookbook contains recipes for configuring a Chef Server instance on a NeCTAR virtual, or similar.

Recipe - default
================

This recipe uses the standard Opscode "chef-server" recipe to create a Chef Server instance on this virtual.  It also sets up cron jobs to:

* perform daily backups of the Chef Server's critical state, and 
* do daily maintenance of the CouchDB service.

Note that:

* This recipe is only viable for platforms for which "Chef Server Omnibus" packages are available.
* Chef Server requires (at least) port 443 to be open.
* By default, this recipe will install the "latest" Omnibus version of Chef Server available.

Attributes
----------

See https://github.com/opscode-cookbooks/chef-server/blob/master/README.md.

Note that further Chef Server options can be specified via the 'configuration' hash, as described in the README.

