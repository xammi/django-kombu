=========================================================
django-kombu - Kombu transport using the Django database.
=========================================================

:version: 0.9.4

Deprecated
==========

django-kombu has now moved into Kombu core, so this repository
is no longer in use.

To upgrade, install the latest Kombu version and add the following
to your settings.py::

    INSTALLED_APPS = (
        "kombu.transport.django",
    )

You can remove the previous "djkombu" entry.


**ORIGINAL README BELOW**


Introduction
============

This package enables you to use the Django database as the message store
for `Kombu`_.


To use you first have to add ``djkombu`` to ``INSTALLED_APPS``, and then
execute ``syncdb`` to create the tables.

``django-kombu`` contains a single transport,
``djkombu.transport.DatabaseTransport``, which is used like this::

    >>> from kombu.connection import BrokerConnection
    >>> c = BrokerConnection(transport="djkombu.transport.DatabaseTransport")


.. _`Kombu`: http://pypi.python.org/pypi/kombu

Installation
============

You can install ``django-kombu`` either via the Python Package Index (PyPI)
or from source.

To install using ``pip``,::

    $ pip install django-kombu


To install using ``easy_install``,::

    $ easy_install django-kombu


If you have downloaded a source tarball you can install it
by doing the following,::

    $ python setup.py build
    # python setup.py install # as root

License
=======

This software is licensed under the ``New BSD License``. See the ``LICENSE``
file in the top distribution directory for the full license text.

.. # vim: syntax=rst expandtab tabstop=4 shiftwidth=4 shiftround

