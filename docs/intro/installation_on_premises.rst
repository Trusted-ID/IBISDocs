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

File system
^^^^^^^^^^^

1.	Copy the installation files to the folder from which the application will be hosted
2.	Edit Connections.config, and alter the connection strings to correspond to your environment
3.	Assign full access permissions for the service account to the following subfolders:

a.	App_Data
b.	App_Content

IIS Manager
^^^^^^^^^^^

1.	Create a new application pool which uses the .NET version specified in the prerequisites
2.	Configure the following settings on the app pool (App pool  Advanced settings):

a.	Start Mode				: AlwaysRunning
b.	Identity				: [service account]
c.	Idle timeout (minutes)		: 0
d.	Maximum worker processes		: 1
e.	Recycling  Regular time interval	: 0

3.	Back in the main screen, right click on the hosting website, and choose Add application
4.	Specify an alias. This is the URL part after the hostname (https://www.server.com/alias)
5.	Set the Application pool to the one created in step 1
6.	Set the physical path to the installation folder, and press OK
7.	Verify that the following feature delegations on the server object are set to Read/Write:

a.	Handler mappings
b.	Modules

8.	Browse to the new application using your favorite web browser (or the one you have available...)
