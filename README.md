[![Dependency Status](https://www.versioneye.com/user/projects/55a9c9ec306535001b00016c/badge.svg?style=flat)](https://www.versioneye.com/user/projects/55a9c9ec306535001b00016c)

# Lucee 5 Application Template for Heroku

Blank application template to deploy [Lucee 5](http://lucee.org) apps on Heroku

---

Find this project useful? [Show some love :revolving_hearts:](https://www.creatorlove.com/mikesprague/lucee-5-heroku-buildpack) and buy me a cup of cofee! :coffee:

---

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

Demo: <https://lucee5.herokuapp.com/> | <https://lucee5.herokuapp.com/test.cfm> | <https://lucee5.herokuapp.com/test.lucee>

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

You should now have Lucee up and running at <http://localhost:5000>. Start adding your code (Lucee code in /src and static files in /pub).

To deploy your site to Heroku you need to setup a free Heroku account, install the Heroku toolbelt (Suggested reading: [Getting Started with Java on Heroku](https://devcenter.heroku.com/articles/getting-started-with-java)). Then..

```bash
$ heroku apps:create [NAME]
$ git push heroku master
$ heroku open
```

You should now be looking at your app running on Heroku.

Enjoy!
