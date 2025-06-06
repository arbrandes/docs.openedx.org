######################
Open edX Lilac Release
######################

.. tags:: site operator

.. warning::

    This release is unsupported.

    The :ref:`Open edX Release Notes` and the :ref:`Open edX Release Notes` are the
    authoratative sources of information on all Open edX releases. It is *strongly*
    recommended to operate off the latest Open edX release at all points in time, as
    only the most recent release is community-supported.

    See the `Open edX Release Schedule`_ for information on release dates and end-of-life
    support.

This section describes how to install the Open edX Lilac release.

.. contents::
 :local:
 :depth: 1

************************
What's Included in Lilac
************************

The Open edX Lilac release contains several new features for learners,
course teams, and developers. For more information, see the
`Open edX Platform Release Notes`__.

__ https://docs.openedx.org/en/latest/community/release_notes/lilac.html


**************************
What Is the Lilac Git Tag?
**************************

A git tag identifies the version of Open edX code that is the Lilac release.
About three dozen repositories are tagged as part of an Open edX release. Many
other repositories are installed as dependencies of those repositories. You can
find the most up-to-date git tag for Lilac on the
:ref:`Open edX Release Notes`.

****************************
Installing the Lilac Release
****************************

.. warning::

    This release is unsupported.

See `Tutor installation instructions <https://docs.tutor.edly.io/gettingstarted.html>`_.

You can install the Open edX Lilac release using the Open edX Installation
instructions (`Tutor`_).

Lilac releases have git tag names like ``open-release/lilac.1``.
The available names are detailed on the :ref:`Open edX Release Notes`.

******************************
Upgrading from the Koa Release
******************************

The recommended approach to upgrading an existing installation of the Open edX
Koa release to the Lilac release is to make a fresh installation of the
Lilac release on a new machine, and move your data and settings to it.

To move and upgrade your Koa data onto a Lilac installation, follow these
steps.

#. Be sure that your Koa installation is on the latest commit from
   ``open-release/koa.master``. This ensures that your database is fully
   migrated and ready for upgrade to Lilac.

#. Stop all services on the Koa machine.

#. Dump the data on the Koa machine. Here's an example script that will dump
   the MySQL and Mongo databases into a single ``.tgz`` file.  The script will
   prompt for the MySQL and Mongo passwords as needed.

    .. code-block:: bash

        #!/bin/bash
        MYSQL_CONN="-uroot -p"
        echo "Reading MySQL database names..."
        mysql ${MYSQL_CONN} -ANe "SELECT schema_name FROM information_schema.schemata WHERE schema_name NOT IN ('mysql','information_schema','performance_schema', 'sys')" > /tmp/db.txt
        DBS="--databases $(cat /tmp/db.txt)"
        NOW="$(date +%Y%m%dT%H%M%S)"
        SQL_FILE="mysql-data-${NOW}.sql"
        echo "Dumping MySQL structures..."
        mysqldump ${MYSQL_CONN} --add-drop-database --skip-add-drop-table --no-data ${DBS} > ${SQL_FILE}
        echo "Dumping MySQL data..."
        # If there is table data you don't need, add --ignore-table=tablename
        mysqldump ${MYSQL_CONN} --no-create-info ${DBS} >> ${SQL_FILE}

        for db in edxapp cs_comments_service; do
            echo "Dumping Mongo db ${db}..."
            mongodump -u admin -p -h localhost --authenticationDatabase admin -d ${db} --out mongo-dump-${NOW}
        done

        tar -czf openedx-data-${NOW}.tgz ${SQL_FILE} mongo-dump-${NOW}

#. Copy the ``.tgz`` data file to the Lilac machine.

#. Stop all services on the Lilac machine.

#. Restore the Koa data into the Lilac machine. As an example, you might
   use the following commands.

    .. code-block:: bash

        $ tar -xvf openedx-data-20200411T154750.tgz
        $ mysql -uroot -p < mysql-data-20200411T154750.sql
        $ mongorestore -u admin -p -h localhost --authenticationDatabase admin --drop -d edxapp mongo-dump-20200411T154750/edxapp
        $ mongorestore -u admin -p -h localhost --authenticationDatabase admin --drop -d cs_comment_service mongo-dump-20200411T154750/cs_comment_service_development

#. Run the Lilac migrations, which will update your Koa data to be
   valid for Lilac:

    .. code-block:: bash

        $ /edx/app/edx_ansible/edx_ansible/util/install/native.sh --tags migrate

#. Copy your configuration files from the Koa machine to the Lilac machine.

#. Restart all services.

***************************************
Upgrading to a Subsequent Lilac Release
***************************************

Occasionally, we release updates to Lilac.  For example, the second
release of Lilac will be ``open-release/lilac.2``.
The steps to upgrade differ based on your original installation method.

===============================
Upgrading a Docker Installation
===============================

Devstack is installed using Docker. To upgrade from one Lilac
release to another, follow the instructions in `devstack`_.

The `devstack`_ installation method is deprecated. It is recommended
to migrate to Tutor. See `Tutor installation instructions <https://docs.tutor.edly.io/gettingstarted.html>`_.

===============================
Upgrading a Native Installation
===============================

If you installed Open edX using the Open edX Native Installation, please
migrate to Tutor. This `Native Installation to Tutor forum post`_ may be helpful,
as may be `this second Native to Tutor post`_. If not, post on the `Open edX Forums`_.

If you installed Open edX using the Open edX Native Installation, you can
upgrade from one Lilac release to another by re-running those steps using
your desired Lilac tag as the new value for ``OPENEDX_RELEASE``.


.. include:: /links.txt


**Maintenance chart**

+--------------+-------------------------------+----------------+------------------------------------+
| Review Date  | Working Group Reviewer        |   Release      |Test situation                      |
+--------------+-------------------------------+----------------+------------------------------------+
| 2025-03-09   | Sarina Canelake               | Sumac          | Deprecated                         |
+--------------+-------------------------------+----------------+------------------------------------+
