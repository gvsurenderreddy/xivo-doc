.. _remote-directory:

****************
Remote directory
****************

If you have a phone provisioned with Wazo and its one of the supported ones, you'll be able to search in your XiVO directory and place call directly
from your phone.

See the list of :ref:`supported devices <supported-devices>` to know if a model supports the XiVO directory or not.


Configuration
=============

For the remote directory to work on your phones, the first thing to do is to go to the
:menuselection:`Services --> IPBX --> (General settings) Phonebook` page.

You then have to add the range of IP addresses that will be allowed to access the directory.
So if you know that your phone's IP addresses are all in the 192.168.1.0/24 subnet, just
click on the small "+" icon and enter "192.168.1.0/24", then save.

You must then restart ``xivo-dird-phoned`` ("Restart Dird server" from the web interface will not
work)::

  systemctl restart xivo-dird-phoned

Once this is done, on your phone, just click on the "remote directory" function key and
you'll be able to do a search in the XiVO directory from it.
