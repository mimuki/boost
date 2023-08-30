# Boost

Boost automatically toots from users of the [Mastodon](https://mastodon.social) social network. Read the documentation in docs/
or [read it online](https://mastodonboost.readthedocs.org/en/latest/).

Forked from <https://gitlab.com/chaica/boost>, but i don't know what I'm doing. I've hacked onto this for my own uses, and maybe that's something you're into. Main changes:

- added config option "dontboostboosts" to only boost, well. boosts
- added config option "dontboostreplies" to only boost replies
- fixed older_than and younger_than config options 

## Tips

if you wanna use this in cron for automated boosting, make sure all your paths are absolute (like, `/home/mimuki/boost/boost.db` and so on).

also i havent really edited the rest of this readme to be accurate or up to date, so good luck. i havent tested this much beyond my very exact use case so stuff might be broken, sorry

## "Quick" Install
Get this repo saved on your computer in the method of your choice (download it and unzip it, clone it, etc). extract it if needed, and run ` python3 setup.py install --install-scripts=/usr/bin`. (or wherever you'd like it to install. just `python3 setup.py install` will install in the current directory.)

Then, run `register_boost_app` to connect up the account you want to boost from, and follow the prompts.

## Use Boost

* Create a boost.ini file in order to configure Boost:

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

        $ boost -c /path/to/boost.ini

## License

This software comes under the terms of the GPLv3+. See the LICENSE file for the complete text of the license.
