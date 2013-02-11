Petri
=====

It's the dough.

![petri](http://us.cdn3.123rf.com/168nwm/prawny/prawny0907/prawny090700015/5159969-a-petri-dish-with-colourful-cartoon-germs-swimming-around-in-it.jpg)

Dependencies
----

* Scss / sass - Install sass, ```gem install sass```
* pip
* virtualenv - ```pip install virtualenv```
* mysql - only used on production, but you need it to install the ```python-mysql``` dependency. To install on osx do a ```brew install mysql```
* sqlite - the database used locally. probably is already installed


Setting up the Database
----

```DJANGO_LOCAL=True ./manage.py syncdb --noinput``` (no need to create a superuser, one will be created for you. see the <a href="#test-users">Test User</a> section.).


Running Locally
----

1. Create a virtualenv in your git directory (don't worry, it will be ignored on checkins) -- ```virtualenv env```
2. Install all the requirements (ensure ```env``` is active by running "env/bin/activate") -- ```pip install -r var/etc/requirements.txt```
3. [optional] Run the celery tasks: ```DJANGO_LOCAL=True ./manage.py celeryd -v 2 -B -E -l INFO``` (this should run in a separate terminal from the server)
4. Run the server in local mode -- ```var/bin/run_local.sh``` or ```DJANGO_LOCAL=True python manage.py runserver```
5. Visit <http://localhost:8000/>

Test Users
----

We automatically create a test user with superuser abilities. Username: ```admin```

The user has the password: "testuser".


Use Cases
----

* [The Hacker Union](http://hackerunion.org), an [open source project](https://github.com/hackerunion/website/), is built on Petri.


Contributors
----

* [Andrew Sass](http://www.andrewsass.com/)
* [Brandon Diamond](http://www.twitter.com/brandondiamond)
* [Matthew Conlen](http://www.mathisonian.com/)



License
----

This project is licensed under GNU GENERAL PUBLIC LICENSE VERSION 3. See the file [LICENSE.md](LICENSE.md) for a copy of the license.

