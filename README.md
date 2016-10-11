[![Dependency Status](https://www.versioneye.com/user/projects/57fcb9c89907da004067f78c/badge.svg?style=flat-square)](https://www.versioneye.com/user/projects/57fcb9c89907da004067f78c)

# Lucee 5 Application Template for Heroku

Blank application template to deploy [Lucee 5](http://lucee.org) apps on Heroku

---

Find this project useful? [Show some love :revolving_hearts:](https://www.creatorlove.com/mikesprague/lucee-5-heroku-buildpack) and buy me a cup of cofee! :coffee:

---

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

Demo: [https://lucee5.herokuapp.com](https://lucee5.herokuapp.com) | [https://lucee5.herokuapp.com/test.cfm](https://lucee5.herokuapp.com/test.cfm)

## Credits/Notes:

- This project is based off of the offical Lucee Heroku Buildpack

## Requirements

- [Maven](http://maven.apache.org/) to build the project
- [Foreman](https://github.com/ddollar/foreman) to run locally

## Instructions

To get started, run the following commands in GitBash (or your terminal of preference):

```bash
$ git clone https://github.com/mikesprague/lucee5-heroku.git
$ cd lucee5-heroku
$ mvn package
$ foreman start
```

NOTE: On Windows, start foreman with the following command:

```bash
$ foreman start -f Procfile.dev
```

You should now have Lucee up and running at <http://localhost:5000>. Start adding your code.

To deploy your site to Heroku you need to setup a free Heroku account, install the Heroku toolbelt (Suggested reading: [Getting Started with Java on Heroku](https://devcenter.heroku.com/articles/getting-started-with-java)). Then...

```bash
$ heroku apps:create [NAME]
$ git push heroku master
$ heroku open
```

You should now be looking at your app running on Heroku.

NOTES:

* If you need access to the admin, disable the first rule in urlrewrite.xml.
* Default password for web admins is `password`. This should be changed to something secure before deploying your app.
* Make any settings (datasources, mail settings, etc.) changes you want locally via the web context, commit your changes and then deploy your app and they will also exist on Heroku.
  * Better practice to add any settings changes, datasources, etc. via Application.cfc; use web context for changes if you must set them via Lucee Admin
  * Server context will be overwritten on deploy, very important desired changes are made to web context if you wish to keep them
* If you get a Heroku application error try reloading the page. This is a known issue. I think the Lucee dependencies aren't quite ready when this happens, I need to look into it further.

Enjoy!

## Known Projects Using the Lucee 5 Application Template for Heroku

Have a project making use of this application template? Lem me know and I'll be happy to list it below!

* [Wheelie CMS](https://github.com/timsayshey/wheelie/) developed by [Tim Badolato (@timsayshey)](https://github.com/timsayshey)
  * CFWheels and Lucee powered CMS with one-click Heroku deploy powered by this project
  * Check out the project repo for full details: [https://github.com/timsayshey/wheelie/](https://github.com/timsayshey/wheelie/)
