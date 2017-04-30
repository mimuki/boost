### Boost

Boost automatically toots from users of the [Mastodon](https://mastodon.social) social network. Read the documentation in docs/
or [read it online](https://boost.readthedocs.org/en/latest/).

If you would like, you can [support the development of this project on Liberapay](https://liberapay.com/carlchenet/).
Alternatively you can donate cryptocurrencies:

- BTC: 139vtPcgzgHxwsC5T4wqwJ6D6N3p969pZL
- XMR: 43GGv8KzVhxehv832FWPTF7FSVuWjuBarFd17QP163uxMaFyoqwmDf1aiRtS5jWgCiRsi73yqedNJJ6V1La2joznKHGAhDi

### Quick Install

* Install Boost from PyPI

        # pip3 install boost

* Install Boost from sources    
  *(see the installation guide for full details)
  [Installation Guide](http://boost.readthedocs.org/en/latest/install.html)*
  

        # tar zxvf boost-0.1.tar.gz
        # cd boostet
        # python3 setup.py install
        # # or
        # python3 setup.py install --install-scripts=/usr/bin

### Use Boost

* Create or modify boost.ini file in order to configure Boost:

        [mastodon]
        users_to_boost=someone@mastodon.social,someonelse@framapiarg.org
        instance_url=https://mastodon.social
        user_credentials=boost_usercred.txt
        client_credentials=boost_clientcred.txt

        [boost]
        boosts=0
        waitminsecs=60
        waitmaxsecs=600
        do_not_boost_hashtags=dnr,
        only_if_hashtags=python,
        match=[Rr]egex
        favorite=true

        [sqlite]
        sqlitepath=/var/lib/boost/boost.db

* Launch Boost

        $ boost /path/to/boost.ini

### Authors

Carl Chenet <chaica@ohmytux.com>

### License

This software comes under the terms of the GPLv3+. See the LICENSE file for the complete text of the license.
