travis ticket 6124
==================

|Build Status|


travis claims :

.. code-block:: yaml

    language: python
    group: travis_latest
    dist: xenial
    sudo: true

    addons:
        apt:
            packages:
                - xvfb

    service:
      - xvfb

    script:
      - service xvfb status         # we would expect the service is started - but it is not
      - sudo service xvfb start     # so start it manually
      - service xvfb status         # and check again


.. see : http://docutils.sourceforge.net/docs/ref/rst/directives.html
.. unfortunately that does not work on github
.. include:: .travis.yml
    :code: yaml


please check : https://travis-ci.org/bitranox/travis6124/builds/518517440

.. |Build Status| image:: https://travis-ci.org/bitranox/travis6124.svg?branch=master
   :target: https://travis-ci.org/bitranox/travis6124
