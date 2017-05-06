Use Boost
=========
After the configuration of Boost, just launch the following command::

    $ boost -c /path/to/boost.ini

Using the --dry-run command line option allows not boosting the toots and not feed local SQLite database, for testing purpose::

    $ boost --dry-run -c /path/to/boost.ini

First time you launch Boost, you may want to avoid to boost the last 20 entries of each user. Use --populate-database option of the command line for that::

    $ boost --populate-database -c /path/to/boost.ini
