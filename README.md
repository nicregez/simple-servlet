simple-servlet
==============

Build
-----

    $ mvn package

Push and Scale
--------------

    $ cf push simple-servlet -m 786mb -p target/simple-servlet-0.1.0-SNAPSHOT.war --random-route
    $ cf scale simple-servlet -i 2
    $ cf apps
    $ cf app simple-servlet

Use
---

Put the randomly generated route into variable URL for ease of use

    $ URL=...
    $ curl http://${URL}/hello

Clean up
--------

Delete the application

    $ cf delete simple-servlet -f
