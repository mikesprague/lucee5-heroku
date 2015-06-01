[![Dependency Status](https://www.versioneye.com/user/projects/556cc5806365320015074a00/badge.svg?style=flat)](https://www.versioneye.com/user/projects/556cc5806365320015074a00)

##Lucee 5 Application Template for Heroku
Blank application template to deploy [Lucee 5](http://lucee.org) apps on Heroku via [Undertow](http://undertow.io/)/[RunWAR](https://github.com/cfmlprojects/runwar)

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

Demo: [https://lucee5.herokuapp.com/](https://lucee5.herokuapp.com/) | [https://lucee5.herokuapp.com/test.cfm](https://lucee5.herokuapp.com/test.cfm) | [https://lucee5.herokuapp.com/test.lucee](https://lucee5.herokuapp.com/test.lucee)

####Credits/Notes:
* This project uses the [cfmlprojects.org](http://cfmlprojects.org/artifacts/org/lucee/) Maven repo maintained by [Denny Valliant](https://github.com/denuno). Many thanks to Denny for his work maintaining cfmlprojects.org.
* You can also check out my version, with an older build style, running Lucee 4.5.x via Winstone on Heroku [https://github.com/mikesprague/lucee-heroku-template](https://github.com/mikesprague/lucee-heroku-template)

###Requirements
* [Maven](http://maven.apache.org/) to build the project
* [Foreman](https://github.com/ddollar/foreman) to run locally

###Instructions
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

You should now have Lucee up and running at [http://localhost:5000](http://localhost:5000).
Start adding your code (Lucee code in /src and static files in /pub).

To deploy your site to Heroku you need to setup a free Heroku account, install the Heroku toolbelt (Suggested reading: [Getting Started with Java on Heroku](https://devcenter.heroku.com/articles/getting-started-with-java)). Then..

```bash
$ heroku apps:create [NAME]
$ git push heroku master
$ heroku open
```

You should now be looking at your app running on Heroku.

Enjoy!
