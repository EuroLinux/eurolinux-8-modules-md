---
document: modulemd
version: 2
data:
  name: python36
  stream: 3.6
  version: '8030020200515150628'
  context: 24f1489c
  arch: x86_64
  license:
    content:
    - ASL 2.0
    - ASL 2.0 and MIT
    - BSD
    - BSD and Boost and Public Domain
    - BSD and LGPLv2+
    - LGPLv2+ and Public Domain
    - MIT
    - Public Domain and BSD and Python and GPLv3+
    - Python
    module:
    - MIT
  summary: Python programming language, version 3.6
  description: 'This module gives users access to the internal Python 3.6 in RHEL8,
    as

    well as provides some additional Python packages the users might need.

    In addition to these you can install any python3-* package available

    in RHEL and use it with Python from this module.'
  dependencies:
  - buildrequires:
      mongodb:
      - 3.6
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      python36:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        rationale: Contains the symlink to the platform-python interpreter. Also contains
          python36-rpm-macros needed to build the remaining packages.
        ref: stream-3.6-rhel-8.3.0
  api:
    rpms:
    - python-sqlalchemy-doc
    - python-virtualenv-doc
    - python3-PyMySQL
    - python3-bson
    - python3-distro
    - python3-docs
    - python3-docutils
    - python3-nose
    - python3-pygments
    - python3-scipy
    - python3-sqlalchemy
    - python3-virtualenv
    - python3-wheel
    - python36
    - python36-debug
    - python36-devel
    - python36-rpm-macros
  buildopts:
    rpms:
      macros: '%_without_python2 1


        # For packages depending on python36, so that they

        # BuildRequire python36-devel/debug/rpm-macros instead of python3-*

        #

        # This won''t be necessary for python37 and later. There we can

        # set %{python3_pkgversion}, because all packages will need to

        # have the pythonXY prefix. Whereas for Python 3.6 the packages

        # are split between non-modular RHEL and the python36 module,

        # and so it was easier and less confusing to keep the prefix at

        # python3- except for the devel/debug/rpm/macros packages.

        %_with_python36_module 1

        '
  references:
    community: https://www.python.org/
    documentation: https://docs.python.org/3.6/
  profiles:
    build:
      rpms:
      - python36
      - python36-devel
      - python36-rpm-macros
    common:
      rpms:
      - python36
  filter:
    rpms:
    - python2-PyMySQL
    - python2-docutils
    - python2-nose
    - python2-pygments
    - python2-scipy
    - python2-sqlalchemy
    - python2-virtualenv
  artifacts:
    rpms:
    - python36-0:3.6.8-2.el8.i686
    - python36-devel-0:3.6.8-2.el8.i686
    - python36-debug-0:3.6.8-2.el8.i686
    - python36-rpm-macros-0:3.6.8-2.el8.noarch
...
