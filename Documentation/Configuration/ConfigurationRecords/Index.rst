﻿

.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. ==================================================
.. DEFINE SOME TEXTROLES
.. --------------------------------------------------
.. role::   underline
.. role::   typoscript(code)
.. role::   ts(typoscript)
   :class:  typoscript
.. role::   php(code)
.. _backend-configuration-record:

Configuration records
^^^^^^^^^^^^^^^^^^^^^

Formerly configuration was done by using pageTS (see below). This is
still possible (fully backwards compatible) but not recommended.
Instead of writing pageTS simply create a configuration record (table:
tx\_crawler\_configuration) and put it on the topmost page of the
pagetree you want to affect with this configuration.

The fields in these records are related to the page ts keys described
below.

Fields and their pageTS equivalents
'''''''''''''''''''''''''''''''''''

- **Name** - corresponds to the "key" part in the pageTS setup
  e.g. tx_crawler.crawlerCfg.paramSets.myConfigurationKeyName

- **Protocol for crawling** - force HTTP, HTTPS or keep the configured protocol

- **Processing instruction filter** - :ref:`paramSets.[key].procInstrFilter <crawler-tsconfig-paramSets-key-procInstrFilter>`

- **Baseurl** - set baseUrl (most likely the same as the entry point configured in your site configuration)

- **Baseurl from Domainrecord** - :ref:`paramSets.[key].baseUrl <crawler-tsconfig-paramSets-key-baseUrl>`

- **Configuration** - :ref:`paramSets.[key] <crawler-tsconfig-paramSets-key>`

- **Page Id of TypoScript root template**

- **Pids only** - :ref:`paramSets.[key].pidsonly <crawler-tsconfig-paramSets-key-pidsonly>`

- **Configuration**

- **Processing instruction parameters**

- **Restrict access to** - restricts access to this configuration record to selected backend user groups. Empty means no restriction is set.

- **Crawl with FE usergroups** - :ref:`paramSets.[key].userGroups <crawler-tsconfig-paramSets-key-userGroups>`

- **Exclude pages** - comma separated list of page ids which should not be crawled

.. image:: /Images/backend_configurationrecord_1.png
.. image:: /Images/backend_configurationrecord_2.png
.. image:: /Images/backend_configurationrecord_3.png

