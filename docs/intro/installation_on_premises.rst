On premises
===========

IBIS runs as an IIS application with an SQL server database. Therefore it needs:

* a service account (Active Directory, not required but strongly recommended)
* an IIS application pool
* an IIS website with an application
* an empty SQL server database

- a DNS record (optional but recommended)
- an SSL certificate (optional but recommended)

We are not going to explain the installation of IIS and/or SQL and the creation of the IIS and/or SQL objects. Requirements are described in the Installation prerequisites document.

.. note:: Authentication and/or authorization errors will most likely occur after installation in case you decide to host the application from a folder outside of C:\Inetpub\wwwroot. These errors are caused by incorrect permissions on the installation folder. In case this happens, copy the permissions of C:\Inetpub\wwwroot to the installation folder