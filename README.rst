Please read the documentation available here:
http://trac.mapfish.org/trac/mapfish/wiki/PrintModuleDoc


Build
-----

Execute the following command():

.. code::

  > ./gradlew build

This will build three artifacts:  print-servlet-xxx.war, print-lib.jar, print-standalone.jar


Deploy
------

The following command will build and upload all artifacts to the maven central repository.

.. code::

  > ./gradlew uploadArchives -DsshPassphrase=...


To use in Eclipse
-----------------

Create Eclipse project metadata:

.. code::

  > ./gradlew eclipse
  
Import project into Eclipse


Run from commandline
--------------------

The following command will run the mapfish printer.  If you do no supply any -Dxxx args then all argument options will be listed.

.. code::

  > ./gradlew print -Dconfig=samples/config.yaml -Dspec=samples/spec.json -Doutput=/tmp/print-out.pdf


Run in Eclipse
--------------

- Create new Java Run Configuration
- Main class is org.mapfish.print.cli.Main
- Program arguments: -config samples/config.yaml -spec samples/spec.json -output $HOME/print.pdf