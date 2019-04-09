Events
======

Content Created
^^^^^^^^^^^^^^^

This event fires when a new object is created in the system. The object itself is added as workflow content and available with the data lookup expressions ( {propertyname} ).

======= ============================
Results
====================================
Done    The incoming object corresponds to the type specified in the activity configuration
======= ============================

============= ======== ====================
Configuration
===========================================
Content type  Required  The type of object to act on. If the incoming object does not correspond to this type the workflow will not be executed 
============= ======== ====================

Content Updated
^^^^^^^^^^^^^^^

This event fires when an object is updated in the system. The object itself is added as workflow content and available with the data lookup expressions ( {propertyname} ).

======= ============================
Results
====================================
Done    The incoming object corresponds to the type specified in the activity configuration
======= ============================

============= ======== ====================
Configuration
===========================================
Content type  Required  The type of object to act on. If the incoming object does not correspond to this type the workflow will not be executed 
Mode          Required  Defines the way to handle property changes:

                            - AND : All specified properties must be changed
                            - OR  : Any of the specified properties must be changed
property      Optional  Defines the properties to filter on in combination with the Mode setting. If specified, the workflow will only be executed when on or more of these properties have changed
============= ======== ====================