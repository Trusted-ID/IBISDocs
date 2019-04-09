Azure
=====

IBIS runs in an Azure App Service. An Azure SQL database is needed for storage. 
Requirements are described in the Installation prerequisites document.

1. Copy the installation files to your Azure App Service

2. Edit Connections.config, and alter the connection strings to correspond to your environment

3. Browse to the new application using your favorite web browser (or the one you have available..)

.. note:: In order to use Azure AD groups for IBIS authorization you need to make a change in your application registration. To do this: 

    1.	Open your application registration in the Azure portal 
    2.	In your application page, click on "Manifest" to open the inline manifest editor 
    3.	Edit the manifest by locating the "groupMembershipClaims" setting and set its value to "SecurityGroup" 
    4.	Save the manifest