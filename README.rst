OXID eShop edition related facts
================================

This component provides eShop editions related information/facts with the help
of `eshop-facts <https://github.com/OXID-eSales/eshop-facts>`__. Information
on how to use ``oe-eshop-edition_facts`` script together with ``oe-eshop-facts``
can be found in the following
`README <https://github.com/OXID-eSales/eshop-facts/blob/master/README.rst>`__.

Output
------

The following information is provided after executing the script:

* ``ESHOP_PE_ROOT_PATH`` - Full path to eShop's Professional edition run-time
  files;
* ``ESHOP_EE_ROOT_PATH`` - Full path to eShop's Enterprise edition run-time
  files;
* ``ESHOP_GET_EDITION_SCRIPT_PATH`` - Full path to a script which retrieves
  the current active edition of eShop's installation;
* ``ESHOP_EDITION`` - Current active eShop edition;
* ``MIGRATION_SUITE`` - eShop edition which is targeted by script execution
  (by default it has an empty value and one must override this to make an
  effect);

Keep in mind that it's possible to override any variable from the list above
by providing it as an environment variable, e.g. to change the path of eShop
PE run-time:

``ESHOP_PE_ROOT_PATH=/var/www/oxideshop/pe ./vendor/bin/oe-eshop-facts oe-eshop-edition_facts``

Input
-----

The following environment variables are accepted:

* ``VERBOSE`` - Enables verbose mode which prints out all facts to ``STDOUT``;
* ``ESHOP_VERBOSE_EDITION_FACTS`` - Enables verbose mode only for the current
  script.
