---
document: modulemd
version: 2
data:
  name: satellite-5-client
  stream: 1.0
  version: '8010020190621091459'
  context: cdc1202b
  arch: x86_64
  license:
    content:
    - GPLv2
    module:
    - MIT
  summary: Red Hat Satellite 5 client packages
  description: Red Hat Satellite 5 client packages provide programs and libraries
    to allow your system to receive software updates from Red Hat Satellite 5.
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      dnf-plugin-spacewalk:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        rationale: DNF plugin for communication with Red Hat Satellite 5.
        ref: rhel-8.0
      rhn-client-tools:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        rationale: Binaries to allow system to receive software updates from Red Hat
          Satellite 5.
        ref: rhel-8.0
      rhnlib:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        rationale: Libraries to allow system to receive software updates from Red
          Hat Satellite 5.
        ref: rhel-8.0
      rhnsd:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        rationale: Red Hat Satellite update agent.
        ref: rhel-8.0
  references:
    community: https://github.com/spacewalkproject/spacewalk/
    documentation: https://access.redhat.com/documentation/en-us/red_hat_satellite/5.8/
    tracker: https://bugzilla.redhat.com/
  profiles:
    common:
      rpms:
      - dnf-plugin-spacewalk
      - rhn-client-tools
      - rhn-setup
      - rhnlib
      - rhnsd
    gui:
      rpms:
      - dnf-plugin-spacewalk
      - rhn-client-tools
      - rhn-setup
      - rhn-setup-gnome
      - rhnlib
      - rhnsd
  artifacts:
    rpms:
    - rhnsd-0:5.0.35-3.module+el8.1.0+3455+3ddf2832.x86_64
    - rhnsd-debugsource-0:5.0.35-3.module+el8.1.0+3455+3ddf2832.x86_64
    - rhnsd-debuginfo-0:5.0.35-3.module+el8.1.0+3455+3ddf2832.x86_64
    - rhnlib-0:2.8.6-8.module+el8.1.0+3455+3ddf2832.noarch
    - python3-rhnlib-0:2.8.6-8.module+el8.1.0+3455+3ddf2832.noarch
    - rhn-client-tools-0:2.8.16-13.module+el8.1.0+3455+3ddf2832.x86_64
    - python3-rhn-client-tools-0:2.8.16-13.module+el8.1.0+3455+3ddf2832.x86_64
    - rhn-check-0:2.8.16-13.module+el8.1.0+3455+3ddf2832.x86_64
    - python3-rhn-check-0:2.8.16-13.module+el8.1.0+3455+3ddf2832.x86_64
    - rhn-setup-0:2.8.16-13.module+el8.1.0+3455+3ddf2832.x86_64
    - python3-rhn-setup-0:2.8.16-13.module+el8.1.0+3455+3ddf2832.x86_64
    - rhn-setup-gnome-0:2.8.16-13.module+el8.1.0+3455+3ddf2832.x86_64
    - python3-rhn-setup-gnome-0:2.8.16-13.module+el8.1.0+3455+3ddf2832.x86_64
    - dnf-plugin-spacewalk-0:2.8.5-11.module+el8.1.0+3455+3ddf2832.noarch
    - python3-dnf-plugin-spacewalk-0:2.8.5-11.module+el8.1.0+3455+3ddf2832.noarch
...
---
document: modulemd
version: 2
data:
  name: python27
  stream: 2.7
  version: '8030020200819165638'
  context: 851f4228
  arch: x86_64
  license:
    content:
    - ASL 2.0
    - ASL 2.0 and MIT
    - ASL 2.0 and MIT and (MIT or GPL)
    - BSD
    - BSD and Boost and Public Domain
    - BSD and Python
    - BSD and Python and Unicode
    - LGPLv2
    - LGPLv2+ and Public Domain
    - LGPLv3+ with exceptions
    - MIT
    - MIT and Public Domain
    - MIT and Python and ASL 2.0 and BSD and ISC and LGPLv2 and MPLv2.0 and (ASL 2.0
      or BSD)
    - Public Domain
    - Public Domain and BSD and Python and GPLv3+
    - Python
    module:
    - MIT
  summary: Python programming language, version 2.7
  description: 'This module provides the Python 2.7 interpreter and additional Python

    packages the users might need.'
  dependencies:
  - buildrequires:
      platform:
      - el8.3.0
      python27:
      - 2.7
    requires:
      platform:
      - el8
  components:
    rpms:
      Cython:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Language for writing Python extension modules. Build dependency
          of numpy and PyYAML
        ref: stream-0.28.1-rhel-8.3.0
      PyYAML:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: YAML parser and emitter for Python
        ref: stream-3.12-rhel-8.3.0
      babel:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Tools for internationalizing Python applications
        ref: stream-2.5.1-rhel-8.3.0
      numpy:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: A fast multidimensional array facility for Python
        ref: stream-1.14.2-rhel-8.3.0
      pytest:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Simple powerful testing with Python
        ref: stream-3.4.2-rhel-8.3.0
      python-PyMySQL:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Python adapter for the MySQL/MariaDB databases
        ref: stream-0.8.0-rhel-8.3.0
      python-attrs:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Python attributes without boilerplate
        ref: stream-17.4.0-rhel-8.3.0
      python-chardet:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Character encoding auto-detection in Python. Dependency of requests.
        ref: stream-3.0.4-rhel-8.3.0
      python-coverage:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Code coverage testing module for Python
        ref: stream-4.5.1-rhel-8.3.0
      python-dns:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: DNS toolkit for Python. Useful package for IPA and mailman.
        ref: stream-1.15.0-rhel-8.3.0
      python-docs:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Documentation for Python
        ref: stream-2.7-rhel-8.3.0
      python-docutils:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: System for processing plaintext documentation
        ref: stream-0.14-rhel-8.3.0
      python-funcsigs:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Python function signatures from PEP362 for Python 2.6, 2.7 and
          3.2+. Dependency of Pytest and mock.
        ref: stream-1.0.2-rhel-8.3.0
      python-idna:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Internationalized Domain Names in Applications (IDNA). Dependency
          of requests.
        ref: stream-2.5-rhel-8.3.0
      python-ipaddress:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Port of the python 3.3+ ipaddress module to 2.6+. Dependency of
          urllib3/requests.
        ref: stream-1.0.18-rhel-8.3.0
      python-jinja2:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: General purpose template engine
        ref: stream-2.10-rhel-8.3.0
      python-lxml:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: XML processing library
        ref: stream-4.2.3-rhel-8.3.0
      python-markupsafe:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Implements a XML/HTML/XHTML Markup safe string for Python
        ref: stream-0.23-rhel-8.3.0
      python-mock:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: A Python Mocking and Patching Library for Testing
        ref: stream-2.0.0-rhel-8.3.0
      python-nose:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Discovery-based unit test extension for Python
        ref: stream-1.3.7-rhel-8.3.0
      python-pluggy:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: The plugin manager stripped of pytest specific details
        ref: stream-0.6.0-rhel-8.3.0
      python-psycopg2:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Python adapter for the PostgreSQL database
        ref: stream-2.7.4-rhel-8.3.0
      python-py:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Library with cross-python path, ini-parsing, io, code, log facilities
        ref: stream-1.5.3-rhel-8.3.0
      python-pygments:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Syntax highlighting engine written in Python
        ref: stream-2.2.0-rhel-8.3.0
      python-pymongo:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Python driver for MongoDB
        ref: stream-3.6.1-rhel-8.3.0
      python-pysocks:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: A Python SOCKS client module. Dependency of urllib3/requests.
        ref: stream-1.6.8-rhel-8.3.0
      python-pytest-mock:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Thin-wrapper around the mock package for easier use with py.test.
          Build dependency of requests.
        ref: stream-1.9.0-rhel-8.3.0
      python-requests:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: HTTP library, written in Python, for human beings
        ref: stream-2.20.0-rhel-8.3.0
      python-setuptools_scm:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Blessed package to manage your versions by scm tags. Build dependency
          of pytest and pytest-mock.
        ref: stream-1.15.7-rhel-8.3.0
      python-six:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Python 2 and 3 compatibility utilities
        ref: stream-1.11.0-rhel-8.3.0
      python-sqlalchemy:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Modular and flexible ORM library for python
        ref: stream-1.3.2-rhel-8.3.0
      python-virtualenv:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Tool to create isolated Python environments
        ref: stream-15.1.0-rhel-8.3.0
      python-wheel:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Used for unbundling of pip and setuptools
        ref: stream-0.30.0-rhel-8.3.0
      python2:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Main Python language interpreter
        ref: stream-2.7-rhel-8.3.0
      python2-pip:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Python Packaging ecosystem
        ref: stream-9.0.3-rhel-8.3.0
      python2-rpm-macros:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Python 2 RPM macros - dependency of python2-devel
        ref: stream-python27-rhel-8.3.0
      python2-setuptools:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Python Packaging ecosystem
        ref: stream-39.0.1-rhel-8.3.0
      pytz:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Runtime requires of babel, and python2-babel
        ref: stream-2017.2-rhel-8.3.0
      scipy:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Scientific Tools for Python
        ref: stream-1.0.0-rhel-8.3.0
  api:
    rpms:
    - babel
    - python-sqlalchemy-doc
    - python2
    - python2-Cython
    - python2-PyMySQL
    - python2-attrs
    - python2-babel
    - python2-backports
    - python2-backports-ssl_match_hostname
    - python2-bson
    - python2-chardet
    - python2-coverage
    - python2-debug
    - python2-devel
    - python2-dns
    - python2-docs
    - python2-docs-info
    - python2-docutils
    - python2-funcsigs
    - python2-idna
    - python2-ipaddress
    - python2-jinja2
    - python2-libs
    - python2-lxml
    - python2-markupsafe
    - python2-mock
    - python2-nose
    - python2-numpy
    - python2-numpy-doc
    - python2-numpy-f2py
    - python2-pip
    - python2-pluggy
    - python2-psycopg2
    - python2-psycopg2-debug
    - python2-psycopg2-tests
    - python2-py
    - python2-pygments
    - python2-pymongo
    - python2-pymongo-gridfs
    - python2-pysocks
    - python2-pytest
    - python2-pytest-mock
    - python2-pytz
    - python2-pyyaml
    - python2-requests
    - python2-rpm-macros
    - python2-scipy
    - python2-setuptools
    - python2-setuptools_scm
    - python2-six
    - python2-sqlalchemy
    - python2-test
    - python2-tkinter
    - python2-tools
    - python2-urllib3
    - python2-virtualenv
    - python2-wheel
  buildopts:
    rpms:
      macros: '# Note that we cannot disable building of all Python 3 subpackages,

        # because python2-devel (needed to build all Python 2 packages)

        # has a runtime dependency on python3-rpm-generators, and that

        # package requires python3-setuptools at runtime. By rebuilding

        # python-setuptools SRPM with only python2, we overshadow the

        # already built python3 subpackage and it is no longer

        # available for python3-rpm-generators when building python-pip

        # (or any other Python package).

        # We can disable Python 3 in all packages but ...

        %_without_python3 1

        # ... we have to have a way to enable some of them as described

        # above. With this macro, we can add some module-specific

        # conditions for python3-* subpackages and other special cases.

        # %_with_python27_module 1


        # for: python-jinja2

        %_with_python2 1


        # to solve circular dependency between pytest and [attrs, pluggy]

        # %_without_tests 1

        '
  references:
    community: https://www.python.org/
    documentation: https://docs.python.org/2.7/
  profiles:
    common:
      rpms:
      - python2
      - python2-libs
      - python2-pip
      - python2-setuptools
  filter:
    rpms:
    - python3-Cython
    - python3-PyMySQL
    - python3-PyYAML
    - python3-attrs
    - python3-babel
    - python3-bson
    - python3-chardet
    - python3-coverage
    - python3-docutils
    - python3-idna
    - python3-jinja2
    - python3-markupsafe
    - python3-mock
    - python3-nose
    - python3-numpy
    - python3-numpy-doc
    - python3-numpy-f2py
    - python3-pluggy
    - python3-psycopg2
    - python3-psycopg2-debug
    - python3-psycopg2-tests
    - python3-py
    - python3-pygments
    - python3-pymongo
    - python3-pymongo-gridfs
    - python3-pysocks
    - python3-pytest
    - python3-pytest-mock
    - python3-pytz
    - python3-requests
    - python3-scipy
    - python3-setuptools_scm
    - python3-six
    - python3-sqlalchemy
    - python3-urllib3
    - python3-virtualenv
  artifacts:
    rpms:
    - python2-pytz-0:2017.2-12.module+el8.3.0+7681+f1f02ded.noarch
    - python2-devel-0:2.7.17-2.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-debugsource-0:2.7.17-2.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-numpy-doc-1:1.14.2-13.module+el8.3.0+7681+f1f02ded.noarch
    - python2-pip-wheel-0:9.0.3-18.module+el8.3.0+7681+f1f02ded.noarch
    - python2-rpm-macros-0:3-38.module+el8.3.0+7681+f1f02ded.noarch
    - python2-setuptools-0:39.0.1-12.module+el8.3.0+7681+f1f02ded.noarch
    - python2-pysocks-0:1.6.8-6.module+el8.3.0+7681+f1f02ded.noarch
    - python2-lxml-debuginfo-0:4.2.3-3.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-debug-0:2.7.17-2.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-mock-0:2.0.0-13.module+el8.3.0+7681+f1f02ded.noarch
    - scipy-debugsource-0:1.0.0-20.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-coverage-0:4.5.1-4.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-tkinter-0:2.7.17-2.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-sqlalchemy-0:1.3.2-2.module+el8.3.0+7681+f1f02ded.x86_64
    - python-psycopg2-debugsource-0:2.7.5-7.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-pymongo-0:3.6.1-11.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-attrs-0:17.4.0-10.module+el8.3.0+7681+f1f02ded.noarch
    - python2-jinja2-0:2.10-8.module+el8.3.0+7681+f1f02ded.noarch
    - python2-wheel-1:0.31.1-2.module+el8.3.0+7681+f1f02ded.noarch
    - python2-bson-debuginfo-0:3.6.1-11.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-coverage-debuginfo-0:4.5.1-4.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-babel-0:2.5.1-9.module+el8.3.0+7681+f1f02ded.noarch
    - python2-0:2.7.17-2.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-setuptools-wheel-0:39.0.1-12.module+el8.3.0+7681+f1f02ded.noarch
    - python-pymongo-debuginfo-0:3.6.1-11.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-pytest-0:3.4.2-13.module+el8.3.0+7681+f1f02ded.noarch
    - python2-psycopg2-tests-0:2.7.5-7.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-test-0:2.7.17-2.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-markupsafe-0:0.23-19.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-pymongo-gridfs-0:3.6.1-11.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-psycopg2-debug-0:2.7.5-7.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-debuginfo-0:2.7.17-2.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-pyyaml-0:3.12-16.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-psycopg2-0:2.7.5-7.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-dns-0:1.15.0-10.module+el8.3.0+7681+f1f02ded.noarch
    - python2-lxml-0:4.2.3-3.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-ipaddress-0:1.0.18-6.module+el8.3.0+7681+f1f02ded.noarch
    - python2-pygments-0:2.2.0-20.module+el8.3.0+7681+f1f02ded.noarch
    - python2-Cython-0:0.28.1-7.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-pip-0:9.0.3-18.module+el8.3.0+7681+f1f02ded.noarch
    - python2-requests-0:2.20.0-3.module+el8.3.0+7681+f1f02ded.noarch
    - python2-six-0:1.11.0-5.module+el8.3.0+7681+f1f02ded.noarch
    - python2-numpy-debuginfo-1:1.14.2-13.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-psycopg2-debuginfo-0:2.7.5-7.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-Cython-debuginfo-0:0.28.1-7.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-docs-info-0:2.7.16-2.module+el8.3.0+7681+f1f02ded.noarch
    - python-psycopg2-doc-0:2.7.5-7.module+el8.3.0+7681+f1f02ded.x86_64
    - numpy-debugsource-1:1.14.2-13.module+el8.3.0+7681+f1f02ded.x86_64
    - python-lxml-debugsource-0:4.2.3-3.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-pymongo-debuginfo-0:3.6.1-11.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-docutils-0:0.14-12.module+el8.3.0+7681+f1f02ded.noarch
    - babel-0:2.5.1-9.module+el8.3.0+7681+f1f02ded.noarch
    - python-pymongo-debugsource-0:3.6.1-11.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-PyMySQL-0:0.8.0-10.module+el8.3.0+7681+f1f02ded.noarch
    - python-coverage-debugsource-0:4.5.1-4.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-numpy-f2py-1:1.14.2-13.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-virtualenv-0:15.1.0-19.module+el8.3.0+7681+f1f02ded.noarch
    - Cython-debugsource-0:0.28.1-7.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-pytest-mock-0:1.9.0-4.module+el8.3.0+7681+f1f02ded.noarch
    - python2-bson-0:3.6.1-11.module+el8.3.0+7681+f1f02ded.x86_64
    - python-psycopg2-debuginfo-0:2.7.5-7.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-funcsigs-0:1.0.2-13.module+el8.3.0+7681+f1f02ded.noarch
    - python2-chardet-0:3.0.4-10.module+el8.3.0+7681+f1f02ded.noarch
    - python2-idna-0:2.5-7.module+el8.3.0+7681+f1f02ded.noarch
    - python-sqlalchemy-doc-0:1.3.2-2.module+el8.3.0+7681+f1f02ded.noarch
    - python2-libs-0:2.7.17-2.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-pluggy-0:0.6.0-8.module+el8.3.0+7681+f1f02ded.noarch
    - python2-docs-0:2.7.16-2.module+el8.3.0+7681+f1f02ded.noarch
    - python2-nose-0:1.3.7-30.module+el8.3.0+7681+f1f02ded.noarch
    - python2-py-0:1.5.3-6.module+el8.3.0+7681+f1f02ded.noarch
    - python2-tools-0:2.7.17-2.module+el8.3.0+7681+f1f02ded.x86_64
    - python-nose-docs-0:1.3.7-30.module+el8.3.0+7681+f1f02ded.noarch
    - python2-scipy-0:1.0.0-20.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-numpy-1:1.14.2-13.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-setuptools_scm-0:1.15.7-6.module+el8.3.0+7681+f1f02ded.noarch
    - PyYAML-debugsource-0:3.12-16.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-scipy-debuginfo-0:1.0.0-20.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-pyyaml-debuginfo-0:3.12-16.module+el8.3.0+7681+f1f02ded.x86_64
    - python2-wheel-wheel-1:0.31.1-2.module+el8.3.0+7681+f1f02ded.noarch
    - python2-psycopg2-debug-debuginfo-0:2.7.5-7.module+el8.3.0+7681+f1f02ded.x86_64
...
---
document: modulemd
version: 2
data:
  name: rust-toolset
  stream: rhel8
  version: '8030020200807201053'
  context: d48633fe
  arch: x86_64
  license:
    content:
    - (ASL 2.0 or MIT) and (BSD and MIT)
    - ASL 2.0 or MIT
    module:
    - MIT
  summary: Rust
  description: Rust Toolset
  dependencies:
  - buildrequires:
      llvm-toolset:
      - rhel8
      platform:
      - el8
      rust-toolset:
      - rhel8
    requires:
      llvm-toolset:
      - rhel8
      platform:
      - el8
  components:
    rpms:
      rust:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Rust compiler and tools
        ref: stream-rhel-8-rhel-8.3.0
      rust-toolset:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Meta package for rust-toolset.
        ref: stream-rhel-8-rhel-8.3.0
  api:
    rpms:
    - cargo
    - cargo-doc
    - clippy
    - rls
    - rust
    - rust-analysis
    - rust-doc
    - rust-gdb
    - rust-lldb
    - rust-src
    - rust-std-static
    - rust-toolset
    - rustfmt
  profiles:
    common:
      rpms:
      - rust-toolset
  artifacts:
    rpms:
    - rust-toolset-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
    - rust-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
    - rust-std-static-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
    - rust-debugger-common-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.noarch
    - rust-gdb-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.noarch
    - rust-lldb-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.noarch
    - rust-doc-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
    - cargo-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
    - cargo-doc-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.noarch
    - rustfmt-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
    - rls-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
    - clippy-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
    - rust-src-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.noarch
    - rust-analysis-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
    - rust-debugsource-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
    - rust-debuginfo-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
    - cargo-debuginfo-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
    - rustfmt-debuginfo-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
    - rls-debuginfo-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
    - clippy-debuginfo-0:1.45.2-1.module+el8.3.0+7604+5c4fe027.x86_64
...
---
document: modulemd
version: 2
data:
  name: subversion
  stream: '1.10'
  version: '8030020200519083055'
  context: 9ce6d490
  arch: x86_64
  license:
    content:
    - ASL 2.0
    - Unicode and MIT
    module:
    - MIT
  summary: Apache Subversion
  description: Apache Subversion, a Modern Version Control System
  dependencies:
  - buildrequires:
      httpd:
      - 2.4
      platform:
      - el8
      swig:
      - 3.0
    requires:
      platform:
      - el8
  components:
    rpms:
      libserf:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        rationale: Build dependency.
        ref: stream-v1-rhel-8.3.0
      subversion:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 20
        rationale: Module API.
        ref: stream-1.10-rhel-8.3.0
      utf8proc:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        rationale: Build dependency.
        ref: stream-v2-rhel-8.3.0
  api:
    rpms:
    - mod_dav_svn
    - subversion
    - subversion-devel
    - subversion-libs
  buildopts:
    rpms:
      macros: '%_without_kwallet 1

        %_without_python2 1

        %_with_python3 1

        %_without_bdb 1

        %_without_pyswig 1

        '
  references:
    documentation: http://subversion.apache.org/docs/
    tracker: https://issues.apache.org/jira/projects/SVN
  profiles:
    common:
      rpms:
      - subversion
      - subversion-libs
      - subversion-tools
    server:
      rpms:
      - mod_dav_svn
      - subversion
      - subversion-libs
      - subversion-tools
  filter:
    rpms:
    - libserf-devel
    - python3-subversion
    - subversion-ruby
    - utf8proc-devel
  artifacts:
    rpms:
    - utf8proc-0:2.1.1-5.module+el8.3.0+6671+2675c974.x86_64
    - utf8proc-devel-0:2.1.1-5.module+el8.3.0+6671+2675c974.x86_64
    - utf8proc-debugsource-0:2.1.1-5.module+el8.3.0+6671+2675c974.x86_64
    - utf8proc-debuginfo-0:2.1.1-5.module+el8.3.0+6671+2675c974.x86_64
    - libserf-0:1.3.9-9.module+el8.3.0+6671+2675c974.x86_64
    - libserf-devel-0:1.3.9-9.module+el8.3.0+6671+2675c974.x86_64
    - libserf-debugsource-0:1.3.9-9.module+el8.3.0+6671+2675c974.x86_64
    - libserf-debuginfo-0:1.3.9-9.module+el8.3.0+6671+2675c974.x86_64
    - subversion-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - subversion-libs-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - subversion-devel-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - subversion-gnome-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - mod_dav_svn-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - subversion-perl-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - subversion-javahl-0:1.10.2-3.module+el8.3.0+6671+2675c974.noarch
    - subversion-ruby-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - subversion-tools-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - subversion-debugsource-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - subversion-debuginfo-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - subversion-libs-debuginfo-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - subversion-devel-debuginfo-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - subversion-gnome-debuginfo-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - mod_dav_svn-debuginfo-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - subversion-perl-debuginfo-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - subversion-ruby-debuginfo-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
    - subversion-tools-debuginfo-0:1.10.2-3.module+el8.3.0+6671+2675c974.x86_64
...
---
document: modulemd
version: 2
data:
  name: varnish
  stream: 6
  version: '8030020200530080205'
  context: 30b713e6
  arch: x86_64
  license:
    content:
    - BSD
    module:
    - MIT
  summary: Varnish HTTP cache
  description: Varnish Cache web application accelerator
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      varnish:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Module API.
        ref: stream-6-rhel-8.3.0
      varnish-modules:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: Extension modules.
        ref: stream-6-rhel-8.3.0
  api:
    rpms:
    - varnish
    - varnish-modules
  buildopts:
    rpms:
      macros: '%_without_python2 1

        %_with_python3 1

        '
  references:
    documentation: http://varnish-cache.org/docs/
    tracker: https://github.com/varnishcache/varnish-cache/issues
  profiles:
    common:
      rpms:
      - varnish
      - varnish-modules
  artifacts:
    rpms:
    - varnish-0:6.0.6-2.module+el8.3.0+6843+b3b42fcc.x86_64
    - varnish-devel-0:6.0.6-2.module+el8.3.0+6843+b3b42fcc.x86_64
    - varnish-docs-0:6.0.6-2.module+el8.3.0+6843+b3b42fcc.x86_64
    - varnish-modules-0:0.15.0-5.module+el8.3.0+6843+b3b42fcc.x86_64
    - varnish-modules-debugsource-0:0.15.0-5.module+el8.3.0+6843+b3b42fcc.x86_64
    - varnish-modules-debuginfo-0:0.15.0-5.module+el8.3.0+6843+b3b42fcc.x86_64
...
---
document: modulemd
version: 2
data:
  name: pki-deps
  stream: 10.6
  version: '8030020200527165326'
  context: 30b713e6
  arch: x86_64
  license:
    content:
    - ASL 1.1 and ASL 2.0
    - ASL 2.0
    - ASL 2.0 and (ASL 2.0 or LGPLv2+)
    - ASL 2.0 and LGPLv2+
    - ASL 2.0 and W3C
    - ASL 2.0 and W3C and Public Domain
    - BSD
    - CDDL or GPLv2 with exception
    - CDDL-1.0 or GPLv2 with exceptions
    - CDDL-1.1 and GPLv2 with exceptions
    - CDDL-1.1 or GPLv2
    - CDDL-1.1 or GPLv2 with exceptions
    - MIT and ASL 2.0
    - MPLv1.1 or LGPLv2+ or ASL 2.0
    - MPLv2.0 or GPLv2+ or LGPLv2+
    module:
    - MIT
  summary: PKI Dependencies module for PKI 10.6 or later
  description: A module to contain dependencies for PKI version 10.6 or later.
  dependencies:
  - buildrequires:
      platform:
      - el8.3.0
    requires:
      platform:
      - el8
  components:
    rpms:
      apache-commons-collections:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Apache Commons Collections packages
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      apache-commons-lang:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Apache Commons Lang packages
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      apache-commons-net:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Apache Commons Net packages
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      bea-stax:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: BEA StAX packages
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      fasterxml-oss-parent:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: FasterXML parent pom BuildRequired by jackson-parent.
        ref: stream-rhel-8.1.0-rhel-8.3.0
      glassfish-fastinfoset:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 4
        rationale: Fast XML Information Set package Requires xmlstreambuffer, xsom.
        ref: stream-pki-10.6-rhel-8.3.0
      glassfish-jax-rs-api:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: GlassFish JAX-RS API packages
        ref: stream-pki-10.6-rhel-8.3.0
      glassfish-jaxb:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 5
        rationale: JAXB Reference Implementation BuildRequires istack-commons. Requires
          glassfish-fastinfoset, glassfish-jaxb-api.
        ref: stream-pki-10.6-rhel-8.3.0
      glassfish-jaxb-api:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: GlassFish JAXB API packages
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      jackson-annotations:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 13
        rationale: Jackson Annotations packages
        ref: stream-pki-10.6-rhel-8.3.0
      jackson-bom:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 11
        rationale: Jackson Bill-of-Materials POM packages
        ref: stream-pki-10.6-rhel-8.3.0
      jackson-core:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 12
        rationale: Jackson Core packages
        ref: stream-pki-10.6-rhel-8.3.0
      jackson-databind:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 14
        rationale: Jackson Data-binding packages
        ref: stream-pki-10.6-rhel-8.3.0
      jackson-jaxrs-providers:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 16
        rationale: Jackson JAX-RS Providers packages
        ref: stream-pki-10.6-rhel-8.3.0
      jackson-module-jaxb-annotations:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 15
        rationale: Jackson JAXB Annotations packages
        ref: stream-pki-10.6-rhel-8.3.0
      jackson-parent:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        rationale: Jackson Parent POM packages BuildRequires fasterxml-oss-parent.
        ref: stream-pki-10.6-rhel-8.3.0
      jakarta-commons-httpclient:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Jakarta Commons HTTPClient packages
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      javassist:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Javassist packages
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      msv:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: Multi-Schema Validator Requires relaxngDatatype.
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      pki-servlet-engine:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: PKI Servlet Engine packages
        ref: stream-pki-10.6-rhel-8.3.0
      python-nss:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Python binding for NSS Provides python-nss for pki-base-java.
        ref: stream-pki-10.6-rhel-8.3.0
      relaxngDatatype:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: RELAX NG packages
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      relaxngcc:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 2
        rationale: RELAX NG Compiler Compiler Requires msv.
        ref: stream-rhel-8.0.0-rhel-8.3.0
      resteasy:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 17
        rationale: RESTEasy packages
        ref: stream-pki-10.6-rhel-8.3.0
      slf4j:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Simple Logging Facade for Java Provides slf4j and slf4j-jdk14 for
          pki-base-java.
        ref: stream-maven-3.5-rhel-8.3.0
      stax-ex:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 2
        rationale: StAX API extensions Requires bea-stax.
        ref: stream-pki-10.6-rhel-8.3.0
      velocity:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Velocity packages
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      xalan-j2:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: Xalan packages Provides xalan-j2 for pki-base-java.
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      xerces-j2:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Xerces packages
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      xml-commons-apis:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: XML Commons APIs packages
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      xml-commons-resolver:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: XML Commons Resolver packages
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      xml-stylebook:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: XML Stylebook packages
        ref: stream-javapackages-tools-201801-rhel-8.3.0
      xmlstreambuffer:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 3
        rationale: XML Stream Buffer package Requires stax-ex.
        ref: stream-pki-10.6-rhel-8.3.0
      xsom:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 3
        rationale: XML Schema Object Model (XSOM) Requires relaxngcc.
        ref: stream-rhel-8.0.0-rhel-8.3.0
  buildopts:
    rpms:
      macros: '%_with_xmvn_javadoc 1

        %_without_asciidoc 1

        %_without_avalon 1

        %_without_bouncycastle 1

        %_without_cython 1

        %_without_dafsa 1

        %_without_desktop 1

        %_without_doxygen 1

        %_without_dtd 1

        %_without_eclipse 1

        %_without_ehcache 1

        %_without_emacs 1

        %_without_equinox 1

        %_without_fop 1

        %_without_ftp 1

        %_without_gradle 1

        %_without_groovy 1

        %_without_hadoop 1

        %_without_hsqldb 1

        %_without_itext 1

        %_without_jackson 1

        %_without_jmh 1

        %_without_jna 1

        %_without_jpa 1

        %_without_junit5 1

        %_without_logback 1

        %_without_markdown 1

        %_without_memcached 1

        %_without_memoryfilesystem 1

        %_without_obr 1

        %_without_python 1

        %_without_reporting 1

        %_without_scm 1

        %_without_snappy 1

        %_without_spring 1

        %_without_ssh 1

        %_without_testlib 1

        '
  references:
    community: http://www.dogtagpki.org
    documentation: http://www.dogtagpki.org
    tracker: https://pagure.io/dogtagpki/issues
  filter:
    rpms:
    - apache-commons-collections-javadoc
    - apache-commons-collections-testframework
    - apache-commons-lang-javadoc
    - apache-commons-net-javadoc
    - bea-stax
    - bea-stax-javadoc
    - fasterxml-oss-parent
    - glassfish-fastinfoset-javadoc
    - glassfish-jax-rs-api
    - glassfish-jax-rs-api-javadoc
    - glassfish-jaxb
    - glassfish-jaxb-api-javadoc
    - glassfish-jaxb-bom
    - glassfish-jaxb-bom-ext
    - glassfish-jaxb-codemodel
    - glassfish-jaxb-codemodel-annotation-compiler
    - glassfish-jaxb-codemodel-parent
    - glassfish-jaxb-external-parent
    - glassfish-jaxb-parent
    - glassfish-jaxb-rngom
    - glassfish-jaxb-runtime-parent
    - glassfish-jaxb-txw-parent
    - jackson-annotations-javadoc
    - jackson-bom
    - jackson-core-javadoc
    - jackson-databind-javadoc
    - jackson-jaxrs-providers-datatypes
    - jackson-jaxrs-providers-javadoc
    - jackson-jaxrs-providers-parent
    - jackson-module-jaxb-annotations-javadoc
    - jackson-parent
    - jakarta-commons-httpclient-demo
    - jakarta-commons-httpclient-javadoc
    - jakarta-commons-httpclient-manual
    - jcl-over-slf4j
    - jul-to-slf4j
    - log4j-over-slf4j
    - msv-demo
    - msv-javadoc
    - msv-manual
    - msv-msv
    - msv-rngconv
    - msv-xmlgen
    - msv-xsdlib
    - relaxngDatatype-javadoc
    - relaxngcc
    - relaxngcc-javadoc
    - resteasy-javadoc
    - slf4j-ext
    - slf4j-javadoc
    - slf4j-jcl
    - slf4j-log4j12
    - slf4j-manual
    - slf4j-sources
    - stax-ex-javadoc
    - velocity-demo
    - velocity-javadoc
    - velocity-manual
    - xalan-j2-demo
    - xalan-j2-javadoc
    - xalan-j2-manual
    - xalan-j2-xsltc
    - xerces-j2-demo
    - xerces-j2-javadoc
    - xml-commons-apis-javadoc
    - xml-commons-apis-manual
    - xml-commons-resolver-javadoc
    - xml-stylebook
    - xml-stylebook-demo
    - xml-stylebook-javadoc
    - xmlstreambuffer-javadoc
    - xsom-javadoc
  artifacts:
    rpms:
    - xml-stylebook-0:1.0-0.25.b3_xalan2.svn313293.module+el8.3.0+6805+72837426.noarch
    - xml-stylebook-javadoc-0:1.0-0.25.b3_xalan2.svn313293.module+el8.3.0+6805+72837426.noarch
    - xml-stylebook-demo-0:1.0-0.25.b3_xalan2.svn313293.module+el8.3.0+6805+72837426.noarch
    - xml-commons-resolver-0:1.2-26.module+el8.3.0+6805+72837426.noarch
    - xml-commons-resolver-javadoc-0:1.2-26.module+el8.3.0+6805+72837426.noarch
    - xml-commons-apis-0:1.4.01-25.module+el8.3.0+6805+72837426.noarch
    - xml-commons-apis-manual-0:1.4.01-25.module+el8.3.0+6805+72837426.noarch
    - xml-commons-apis-javadoc-0:1.4.01-25.module+el8.3.0+6805+72837426.noarch
    - xerces-j2-0:2.11.0-34.module+el8.3.0+6805+72837426.noarch
    - xerces-j2-javadoc-0:2.11.0-34.module+el8.3.0+6805+72837426.noarch
    - xerces-j2-demo-0:2.11.0-34.module+el8.3.0+6805+72837426.noarch
    - velocity-0:1.7-24.module+el8.3.0+6805+72837426.noarch
    - velocity-manual-0:1.7-24.module+el8.3.0+6805+72837426.noarch
    - velocity-javadoc-0:1.7-24.module+el8.3.0+6805+72837426.noarch
    - velocity-demo-0:1.7-24.module+el8.3.0+6805+72837426.noarch
    - slf4j-0:1.7.25-4.module+el8.3.0+6805+72837426.noarch
    - slf4j-javadoc-0:1.7.25-4.module+el8.3.0+6805+72837426.noarch
    - slf4j-manual-0:1.7.25-4.module+el8.3.0+6805+72837426.noarch
    - slf4j-jdk14-0:1.7.25-4.module+el8.3.0+6805+72837426.noarch
    - slf4j-log4j12-0:1.7.25-4.module+el8.3.0+6805+72837426.noarch
    - slf4j-jcl-0:1.7.25-4.module+el8.3.0+6805+72837426.noarch
    - slf4j-ext-0:1.7.25-4.module+el8.3.0+6805+72837426.noarch
    - jcl-over-slf4j-0:1.7.25-4.module+el8.3.0+6805+72837426.noarch
    - log4j-over-slf4j-0:1.7.25-4.module+el8.3.0+6805+72837426.noarch
    - jul-to-slf4j-0:1.7.25-4.module+el8.3.0+6805+72837426.noarch
    - slf4j-sources-0:1.7.25-4.module+el8.3.0+6805+72837426.noarch
    - relaxngDatatype-0:2011.1-7.module+el8.3.0+6805+72837426.noarch
    - relaxngDatatype-javadoc-0:2011.1-7.module+el8.3.0+6805+72837426.noarch
    - python3-nss-0:1.0.1-10.module+el8.3.0+6805+72837426.x86_64
    - python-nss-doc-0:1.0.1-10.module+el8.3.0+6805+72837426.x86_64
    - python-nss-debugsource-0:1.0.1-10.module+el8.3.0+6805+72837426.x86_64
    - python3-nss-debuginfo-0:1.0.1-10.module+el8.3.0+6805+72837426.x86_64
    - pki-servlet-engine-1:9.0.30-1.module+el8.3.0+6805+72837426.noarch
    - pki-servlet-4.0-api-1:9.0.30-1.module+el8.3.0+6805+72837426.noarch
    - javassist-0:3.18.1-8.module+el8.3.0+6805+72837426.noarch
    - javassist-javadoc-0:3.18.1-8.module+el8.3.0+6805+72837426.noarch
    - jakarta-commons-httpclient-1:3.1-28.module+el8.3.0+6805+72837426.noarch
    - jakarta-commons-httpclient-javadoc-1:3.1-28.module+el8.3.0+6805+72837426.noarch
    - jakarta-commons-httpclient-demo-1:3.1-28.module+el8.3.0+6805+72837426.noarch
    - jakarta-commons-httpclient-manual-1:3.1-28.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-api-0:2.2.12-8.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-api-javadoc-0:2.2.12-8.module+el8.3.0+6805+72837426.noarch
    - glassfish-jax-rs-api-0:2.0.1-6.module+el8.3.0+6805+72837426.noarch
    - glassfish-jax-rs-api-javadoc-0:2.0.1-6.module+el8.3.0+6805+72837426.noarch
    - fasterxml-oss-parent-0:26-6.module+el8.3.0+6805+72837426.noarch
    - bea-stax-0:1.2.0-16.module+el8.3.0+6805+72837426.noarch
    - bea-stax-api-0:1.2.0-16.module+el8.3.0+6805+72837426.noarch
    - bea-stax-javadoc-0:1.2.0-16.module+el8.3.0+6805+72837426.noarch
    - apache-commons-net-0:3.6-3.module+el8.3.0+6805+72837426.noarch
    - apache-commons-net-javadoc-0:3.6-3.module+el8.3.0+6805+72837426.noarch
    - apache-commons-lang-0:2.6-21.module+el8.3.0+6805+72837426.noarch
    - apache-commons-lang-javadoc-0:2.6-21.module+el8.3.0+6805+72837426.noarch
    - apache-commons-collections-0:3.2.2-10.module+el8.3.0+6805+72837426.noarch
    - apache-commons-collections-testframework-0:3.2.2-10.module+el8.3.0+6805+72837426.noarch
    - apache-commons-collections-javadoc-0:3.2.2-10.module+el8.3.0+6805+72837426.noarch
    - xalan-j2-0:2.7.1-38.module+el8.3.0+6805+72837426.noarch
    - xalan-j2-xsltc-0:2.7.1-38.module+el8.3.0+6805+72837426.noarch
    - xalan-j2-manual-0:2.7.1-38.module+el8.3.0+6805+72837426.noarch
    - xalan-j2-javadoc-0:2.7.1-38.module+el8.3.0+6805+72837426.noarch
    - xalan-j2-demo-0:2.7.1-38.module+el8.3.0+6805+72837426.noarch
    - msv-msv-1:2013.6.1-10.module+el8.3.0+6805+72837426.noarch
    - msv-rngconv-1:2013.6.1-10.module+el8.3.0+6805+72837426.noarch
    - msv-xmlgen-1:2013.6.1-10.module+el8.3.0+6805+72837426.noarch
    - msv-xsdlib-1:2013.6.1-10.module+el8.3.0+6805+72837426.noarch
    - msv-javadoc-1:2013.6.1-10.module+el8.3.0+6805+72837426.noarch
    - msv-manual-1:2013.6.1-10.module+el8.3.0+6805+72837426.noarch
    - msv-demo-1:2013.6.1-10.module+el8.3.0+6805+72837426.noarch
    - stax-ex-0:1.7.7-8.module+el8.3.0+6805+72837426.noarch
    - stax-ex-javadoc-0:1.7.7-8.module+el8.3.0+6805+72837426.noarch
    - relaxngcc-0:1.12-14.module+el8.3.0+6805+72837426.noarch
    - relaxngcc-javadoc-0:1.12-14.module+el8.3.0+6805+72837426.noarch
    - xsom-0:0-19.20110809svn.module+el8.3.0+6805+72837426.noarch
    - xsom-javadoc-0:0-19.20110809svn.module+el8.3.0+6805+72837426.noarch
    - xmlstreambuffer-0:1.5.4-8.module+el8.3.0+6805+72837426.noarch
    - xmlstreambuffer-javadoc-0:1.5.4-8.module+el8.3.0+6805+72837426.noarch
    - glassfish-fastinfoset-0:1.2.13-9.module+el8.3.0+6805+72837426.noarch
    - glassfish-fastinfoset-javadoc-0:1.2.13-9.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-0:2.2.11-11.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-codemodel-0:2.2.11-11.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-codemodel-annotation-compiler-0:2.2.11-11.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-bom-0:2.2.11-11.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-bom-ext-0:2.2.11-11.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-codemodel-parent-0:2.2.11-11.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-core-0:2.2.11-11.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-external-parent-0:2.2.11-11.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-parent-0:2.2.11-11.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-runtime-0:2.2.11-11.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-runtime-parent-0:2.2.11-11.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-txw-parent-0:2.2.11-11.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-rngom-0:2.2.11-11.module+el8.3.0+6805+72837426.noarch
    - glassfish-jaxb-txw2-0:2.2.11-11.module+el8.3.0+6805+72837426.noarch
    - jackson-parent-0:2.10-1.module+el8.3.0+6805+72837426.noarch
    - jackson-bom-0:2.10.0-1.module+el8.3.0+6805+72837426.noarch
    - jackson-core-0:2.10.0-1.module+el8.3.0+6805+72837426.noarch
    - jackson-core-javadoc-0:2.10.0-1.module+el8.3.0+6805+72837426.noarch
    - jackson-annotations-0:2.10.0-1.module+el8.3.0+6805+72837426.noarch
    - jackson-annotations-javadoc-0:2.10.0-1.module+el8.3.0+6805+72837426.noarch
    - jackson-databind-0:2.10.0-1.module+el8.3.0+6805+72837426.noarch
    - jackson-databind-javadoc-0:2.10.0-1.module+el8.3.0+6805+72837426.noarch
    - jackson-module-jaxb-annotations-0:2.7.6-4.module+el8.3.0+6805+72837426.noarch
    - jackson-module-jaxb-annotations-javadoc-0:2.7.6-4.module+el8.3.0+6805+72837426.noarch
    - jackson-jaxrs-providers-0:2.9.9-1.module+el8.3.0+6805+72837426.noarch
    - jackson-jaxrs-json-provider-0:2.9.9-1.module+el8.3.0+6805+72837426.noarch
    - jackson-jaxrs-providers-datatypes-0:2.9.9-1.module+el8.3.0+6805+72837426.noarch
    - jackson-jaxrs-providers-parent-0:2.9.9-1.module+el8.3.0+6805+72837426.noarch
    - jackson-jaxrs-providers-javadoc-0:2.9.9-1.module+el8.3.0+6805+72837426.noarch
    - resteasy-0:3.0.26-3.module+el8.3.0+6805+72837426.noarch
    - resteasy-javadoc-0:3.0.26-3.module+el8.3.0+6805+72837426.noarch
...
---
document: modulemd
version: 2
data:
  name: pki-core
  stream: 10.6
  version: '8030020200911215836'
  context: 5ff1562f
  arch: x86_64
  license:
    content:
    - GPLv2 and LGPLv2
    - LGPLv2+
    - MPLv1.1 or GPLv2+ or LGPLv2+
    module:
    - MIT
  summary: PKI Core module for PKI 10.6 or later
  description: A module for PKI Core packages for PKI version 10.6 or later.
  dependencies:
  - buildrequires:
      golang-ecosystem:
      - 1.0
      pki-deps:
      - 10.6
      platform:
      - el8
    requires:
      pki-deps:
      - 10.6
      platform:
      - el8
  components:
    rpms:
      jss:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: JSS packages
        ref: stream-pki-10.6-rhel-8.3.0
      ldapjdk:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: LDAP JDK packages
        ref: stream-pki-10.6-rhel-8.3.0
      pki-core:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 2
        rationale: PKI Core packages
        ref: stream-pki-10.6-rhel-8.3.0
      tomcatjss:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: TomcatJSS packages
        ref: stream-pki-10.6-rhel-8.3.0
  references:
    community: http://www.dogtagpki.org
    documentation: http://www.dogtagpki.org
    tracker: https://pagure.io/dogtagpki/issues
  artifacts:
    rpms:
    - jss-0:4.7.3-1.module+el8.3.0+8058+d5cd4219.x86_64
    - jss-javadoc-0:4.7.3-1.module+el8.3.0+8058+d5cd4219.x86_64
    - jss-debugsource-0:4.7.3-1.module+el8.3.0+8058+d5cd4219.x86_64
    - jss-debuginfo-0:4.7.3-1.module+el8.3.0+8058+d5cd4219.x86_64
    - tomcatjss-0:7.5.0-1.module+el8.3.0+8058+d5cd4219.noarch
    - ldapjdk-0:4.22.0-1.module+el8.3.0+8058+d5cd4219.noarch
    - ldapjdk-javadoc-0:4.22.0-1.module+el8.3.0+8058+d5cd4219.noarch
    - pki-symkey-0:10.9.4-1.module+el8.3.0+8058+d5cd4219.x86_64
    - pki-base-0:10.9.4-1.module+el8.3.0+8058+d5cd4219.noarch
    - python3-pki-0:10.9.4-1.module+el8.3.0+8058+d5cd4219.noarch
    - pki-base-java-0:10.9.4-1.module+el8.3.0+8058+d5cd4219.noarch
    - pki-tools-0:10.9.4-1.module+el8.3.0+8058+d5cd4219.x86_64
    - pki-server-0:10.9.4-1.module+el8.3.0+8058+d5cd4219.noarch
    - pki-ca-0:10.9.4-1.module+el8.3.0+8058+d5cd4219.noarch
    - pki-kra-0:10.9.4-1.module+el8.3.0+8058+d5cd4219.noarch
    - pki-core-debugsource-0:10.9.4-1.module+el8.3.0+8058+d5cd4219.x86_64
    - pki-core-debuginfo-0:10.9.4-1.module+el8.3.0+8058+d5cd4219.x86_64
    - pki-symkey-debuginfo-0:10.9.4-1.module+el8.3.0+8058+d5cd4219.x86_64
    - pki-tools-debuginfo-0:10.9.4-1.module+el8.3.0+8058+d5cd4219.x86_64
...
---
document: modulemd
version: 2
data:
  name: swig
  stream: 3.0
  version: '8030020200407110056'
  context: 30b713e6
  arch: x86_64
  license:
    content:
    - BSD
    - GPLv3+ and BSD
    module:
    - MIT
  summary: Connects C/C++/Objective C to some high-level programming languages
  description: 'Simplified Wrapper and Interface Generator (SWIG) is a software development
    tool for connecting C, C++ and Objective C programs with a variety of high-level
    programming languages. SWIG is primarily used with Perl, Python and Tcl/TK, but
    it has also been extended to Java, Eiffel and Guile. SWIG is normally used to
    create high-level interpreted programming environments, systems integration, and
    as a tool for building user interfaces

    '
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      swig:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: SWIG package
        ref: stream-3.0-rhel-8.3.0
  api:
    rpms:
    - swig
    - swig-doc
    - swig-gdb
  buildopts:
    rpms:
      macros: '%golang 0

        %guile 0

        %javalang 0

        %lualang 0

        %octave 0

        %phplang 0

        %python2lang 0

        %Rlang 0

        %rubylang 0

        %tcl 0

        %_without_build_ccache_swig 1

        '
  references:
    community: http://swig.org/
    documentation: http://swig.org/doc.html
    tracker: http://bugzilla.redhat.com
  profiles:
    common:
      rpms:
      - swig
    complete:
      rpms:
      - swig
      - swig-doc
      - swig-gdb
  artifacts:
    rpms:
    - swig-debuginfo-0:3.0.12-19.module+el8.3.0+6248+838326ab.x86_64
    - swig-gdb-0:3.0.12-19.module+el8.3.0+6248+838326ab.x86_64
    - swig-doc-0:3.0.12-19.module+el8.3.0+6248+838326ab.noarch
    - swig-debugsource-0:3.0.12-19.module+el8.3.0+6248+838326ab.x86_64
    - swig-0:3.0.12-19.module+el8.3.0+6248+838326ab.x86_64
...
---
document: modulemd
version: 2
data:
  name: ruby
  stream: 2.7
  version: '8030020200626154145'
  context: 30b713e6
  arch: x86_64
  license:
    content:
    - (BSD or Ruby) and PostgreSQL
    - (Ruby or BSD) and (Ruby or BSD or Python) and (Ruby or BSD or LGPLv2+)
    - (Ruby or BSD) and Public Domain and MIT and CC0 and zlib and UCD
    - (Ruby or GPLv2) and UCD
    - ASL 2.0
    - GPLv2 and Ruby and MIT and OFL
    - MIT
    - Ruby or BSD
    - Ruby or MIT
    module:
    - MIT
  summary: An interpreter of object-oriented scripting language
  description: Ruby is the interpreted scripting language for quick and easy object-oriented
    programming.  It has many features to process text files and to do system management
    tasks (as in Perl).  It is simple, straight-forward, and extensible.
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      ruby:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 101
        multilib:
        - x86_64
        rationale: An interpreter of object-oriented scripting language
        ref: stream-ruby-2.7-rhel-8.3.0
      rubygem-abrt:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 102
        rationale: ABRT support for Ruby
        ref: stream-ruby-2.7-rhel-8.3.0
      rubygem-bson:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 102
        rationale: Ruby Implementation of the BSON specification
        ref: stream-ruby-2.7-rhel-8.3.0
      rubygem-mongo:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 103
        rationale: Ruby driver for MongoDB
        ref: stream-ruby-2.7-rhel-8.3.0
      rubygem-mysql2:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 102
        rationale: A simple, fast Mysql library for Ruby, binding to libmysql
        ref: stream-ruby-2.7-rhel-8.3.0
      rubygem-pg:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 102
        rationale: A Ruby interface to the PostgreSQL RDBMS
        ref: stream-ruby-2.7-rhel-8.3.0
  api:
    rpms:
    - ruby
    - ruby-default-gems
    - ruby-devel
    - ruby-libs
    - rubygem-abrt
    - rubygem-bigdecimal
    - rubygem-bson
    - rubygem-bundler
    - rubygem-io-console
    - rubygem-irb
    - rubygem-json
    - rubygem-minitest
    - rubygem-mongo
    - rubygem-mysql2
    - rubygem-net-telnet
    - rubygem-openssl
    - rubygem-pg
    - rubygem-power_assert
    - rubygem-psych
    - rubygem-rake
    - rubygem-rdoc
    - rubygem-test-unit
    - rubygem-xmlrpc
    - rubygems
    - rubygems-devel
  references:
    community: http://ruby-lang.org/
    documentation: https://www.ruby-lang.org/en/documentation/
    tracker: https://bugs.ruby-lang.org/
  profiles:
    common:
      rpms:
      - ruby
  artifacts:
    rpms:
    - rubygem-mongo-doc-0:2.11.3-1.module+el8.3.0+7192+4e3a532a.noarch
    - rubygem-rake-0:13.0.1-133.module+el8.3.0+7192+4e3a532a.noarch
    - rubygem-io-console-debuginfo-0:0.5.6-133.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-mongo-0:2.11.3-1.module+el8.3.0+7192+4e3a532a.noarch
    - rubygem-psych-0:3.1.0-133.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-bundler-0:2.1.4-133.module+el8.3.0+7192+4e3a532a.noarch
    - ruby-doc-0:2.7.1-133.module+el8.3.0+7192+4e3a532a.noarch
    - rubygem-pg-doc-0:1.2.3-1.module+el8.3.0+7192+4e3a532a.noarch
    - rubygem-test-unit-0:3.3.4-133.module+el8.3.0+7192+4e3a532a.noarch
    - rubygem-abrt-doc-0:0.4.0-1.module+el8.3.0+7192+4e3a532a.noarch
    - rubygems-0:3.1.2-133.module+el8.3.0+7192+4e3a532a.noarch
    - rubygem-bson-0:4.8.1-1.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-bigdecimal-debuginfo-0:2.0.0-133.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-xmlrpc-0:0.3.0-133.module+el8.3.0+7192+4e3a532a.noarch
    - rubygem-pg-debuginfo-0:1.2.3-1.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-json-debuginfo-0:2.3.0-133.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-bson-doc-0:4.8.1-1.module+el8.3.0+7192+4e3a532a.noarch
    - rubygem-mysql2-doc-0:0.5.3-1.module+el8.3.0+7192+4e3a532a.noarch
    - rubygem-bigdecimal-0:2.0.0-133.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-mysql2-debuginfo-0:0.5.3-1.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-openssl-debuginfo-0:2.1.2-133.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-net-telnet-0:0.2.0-133.module+el8.3.0+7192+4e3a532a.noarch
    - rubygem-minitest-0:5.13.0-133.module+el8.3.0+7192+4e3a532a.noarch
    - rubygem-bson-debugsource-0:4.8.1-1.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-pg-debugsource-0:1.2.3-1.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-bson-debuginfo-0:4.8.1-1.module+el8.3.0+7192+4e3a532a.x86_64
    - ruby-libs-debuginfo-0:2.7.1-133.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-mysql2-debugsource-0:0.5.3-1.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-mysql2-0:0.5.3-1.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-json-0:2.3.0-133.module+el8.3.0+7192+4e3a532a.x86_64
    - ruby-devel-0:2.7.1-133.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-abrt-0:0.4.0-1.module+el8.3.0+7192+4e3a532a.noarch
    - rubygem-pg-0:1.2.3-1.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-openssl-0:2.1.2-133.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-psych-debuginfo-0:3.1.0-133.module+el8.3.0+7192+4e3a532a.x86_64
    - ruby-default-gems-0:2.7.1-133.module+el8.3.0+7192+4e3a532a.noarch
    - rubygem-io-console-0:0.5.6-133.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-rdoc-0:6.2.1-133.module+el8.3.0+7192+4e3a532a.noarch
    - ruby-0:2.7.1-133.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-power_assert-0:1.1.7-133.module+el8.3.0+7192+4e3a532a.noarch
    - rubygems-devel-0:3.1.2-133.module+el8.3.0+7192+4e3a532a.noarch
    - ruby-debuginfo-0:2.7.1-133.module+el8.3.0+7192+4e3a532a.x86_64
    - ruby-debugsource-0:2.7.1-133.module+el8.3.0+7192+4e3a532a.x86_64
    - rubygem-irb-0:1.2.3-133.module+el8.3.0+7192+4e3a532a.noarch
    - ruby-libs-0:2.7.1-133.module+el8.3.0+7192+4e3a532a.x86_64
...
---
document: modulemd
version: 2
data:
  name: php
  stream: 7.4
  version: '8030020200615123046'
  context: eb6bdfed
  arch: x86_64
  license:
    content:
    - BSD
    - BSD and LGPLv3+
    - PHP
    - PHP and BSD
    - PHP and LGPLv2 and OpenLDAP
    - PHP and LGPLv2+
    - PHP and Zend and BSD and MIT and ASL 1.0 and NCSA
    - PHP and Zend and BSD and MIT and ASL 1.0 and NCSA and PostgreSQL
    module:
    - GPLv2+
  summary: PHP scripting language
  description: php 7.4 module
  dependencies:
  - buildrequires:
      httpd:
      - 2.4
      nginx:
      - 1.14
      platform:
      - el8
    requires:
      httpd:
      - 2.4
      nginx: []
      platform:
      - el8
  components:
    rpms:
      libzip:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: ZIP library
        ref: stream-php-7.4-rhel-8.3.0
      php:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: Module API.
        ref: stream-7.4-rhel-8.3.0
      php-pear:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 2
        rationale: Extension management
        ref: stream-php-7.4-rhel-8.3.0
      php-pecl-apcu:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 3
        rationale: APCu extension
        ref: stream-php-7.4-rhel-8.3.0
      php-pecl-rrd:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 3
        rationale: RRD extension
        ref: stream-php-7.4-rhel-8.3.0
      php-pecl-xdebug:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 3
        rationale: Xdebug extension
        ref: stream-php-7.4-rhel-8.3.0
      php-pecl-zip:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 3
        rationale: ZIP extension
        ref: stream-php-7.4-rhel-8.3.0
  api:
    rpms:
    - php-fpm
  references:
    documentation: http://php.net/
    tracker: https://bugs.php.net/
  profiles:
    common:
      rpms:
      - php-cli
      - php-common
      - php-fpm
      - php-json
      - php-mbstring
      - php-xml
    devel:
      rpms:
      - libzip
      - php-cli
      - php-common
      - php-devel
      - php-fpm
      - php-json
      - php-mbstring
      - php-pear
      - php-pecl-zip
      - php-process
      - php-xml
    minimal:
      rpms:
      - php-cli
      - php-common
  artifacts:
    rpms:
    - php-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-cli-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-dbg-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-fpm-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-common-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-devel-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-opcache-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-ldap-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-pdo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-mysqlnd-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-pgsql-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-process-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-odbc-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-soap-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-snmp-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-xml-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-xmlrpc-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-mbstring-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-gd-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-bcmath-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-gmp-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-dba-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-embedded-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-intl-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-enchant-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-json-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-ffi-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-debugsource-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-cli-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-dbg-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-fpm-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-common-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-opcache-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-ldap-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-pdo-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-mysqlnd-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-pgsql-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-process-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-odbc-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-soap-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-snmp-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-xml-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-xmlrpc-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-mbstring-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-gd-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-bcmath-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-gmp-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-dba-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-embedded-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-intl-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-enchant-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-json-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - php-ffi-debuginfo-0:7.4.6-4.module+el8.3.0+6678+b09f589e.x86_64
    - libzip-0:1.6.1-1.module+el8.3.0+6678+b09f589e.x86_64
    - libzip-devel-0:1.6.1-1.module+el8.3.0+6678+b09f589e.x86_64
    - libzip-tools-0:1.6.1-1.module+el8.3.0+6678+b09f589e.x86_64
    - libzip-debugsource-0:1.6.1-1.module+el8.3.0+6678+b09f589e.x86_64
    - libzip-debuginfo-0:1.6.1-1.module+el8.3.0+6678+b09f589e.x86_64
    - libzip-tools-debuginfo-0:1.6.1-1.module+el8.3.0+6678+b09f589e.x86_64
    - php-pear-1:1.10.12-1.module+el8.3.0+6678+b09f589e.noarch
    - php-pecl-zip-0:1.18.2-1.module+el8.3.0+6678+b09f589e.x86_64
    - php-pecl-zip-debugsource-0:1.18.2-1.module+el8.3.0+6678+b09f589e.x86_64
    - php-pecl-zip-debuginfo-0:1.18.2-1.module+el8.3.0+6678+b09f589e.x86_64
    - php-pecl-xdebug-0:2.9.5-1.module+el8.3.0+6678+b09f589e.x86_64
    - php-pecl-xdebug-debugsource-0:2.9.5-1.module+el8.3.0+6678+b09f589e.x86_64
    - php-pecl-xdebug-debuginfo-0:2.9.5-1.module+el8.3.0+6678+b09f589e.x86_64
    - php-pecl-rrd-0:2.0.1-1.module+el8.3.0+6678+b09f589e.x86_64
    - php-pecl-rrd-debugsource-0:2.0.1-1.module+el8.3.0+6678+b09f589e.x86_64
    - php-pecl-rrd-debuginfo-0:2.0.1-1.module+el8.3.0+6678+b09f589e.x86_64
    - php-pecl-apcu-0:5.1.18-1.module+el8.3.0+6678+b09f589e.x86_64
    - php-pecl-apcu-devel-0:5.1.18-1.module+el8.3.0+6678+b09f589e.x86_64
    - apcu-panel-0:5.1.18-1.module+el8.3.0+6678+b09f589e.noarch
    - php-pecl-apcu-debugsource-0:5.1.18-1.module+el8.3.0+6678+b09f589e.x86_64
    - php-pecl-apcu-debuginfo-0:5.1.18-1.module+el8.3.0+6678+b09f589e.x86_64
...
---
document: modulemd
version: 2
data:
  name: squid
  stream: 4
  version: '8030020200828070549'
  context: 30b713e6
  arch: x86_64
  license:
    content:
    - BSD
    - GPLv2+ and (LGPLv2+ and MIT and BSD and Public Domain)
    module:
    - MIT
  summary: Squid - Optimising Web Delivery
  description: an initial version of the squid caching proxy module
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      libecap:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: library needed by Squid
        ref: stream-1.0-rhel-8.3.0
      squid:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 2
        rationale: squid caching proxy
        ref: stream-4-rhel-8.3.0
  api:
    rpms:
    - squid
  references:
    documentation: http://www.squid-cache.org/Doc/
    tracker: https://bugs.squid-cache.org/index.cgi
  profiles:
    common:
      rpms:
      - squid
  artifacts:
    rpms:
    - libecap-0:1.0.1-2.module+el8.3.0+7851+7808b5f9.x86_64
    - libecap-debugsource-0:1.0.1-2.module+el8.3.0+7851+7808b5f9.x86_64
    - libecap-devel-0:1.0.1-2.module+el8.3.0+7851+7808b5f9.x86_64
    - libecap-debuginfo-0:1.0.1-2.module+el8.3.0+7851+7808b5f9.x86_64
    - squid-7:4.11-3.module+el8.3.0+7851+7808b5f9.x86_64
    - squid-debuginfo-7:4.11-3.module+el8.3.0+7851+7808b5f9.x86_64
    - squid-debugsource-7:4.11-3.module+el8.3.0+7851+7808b5f9.x86_64
...
---
document: modulemd
version: 2
data:
  name: scala
  stream: '2.10'
  version: '820181213143541'
  context: 2b79a98f
  arch: x86_64
  license:
    content:
    - ASL 2.0
    - ASL 2.0 and EPL and BSD
    - BSD
    - BSD and CC0 and Public Domain
    module:
    - MIT
  summary: A hybrid functional/object-oriented language for the JVM
  description: Scala is a general purpose programming language designed to express
    common programming patterns in a concise, elegant, and type-safe way. It smoothly
    integrates features of object-oriented and functional languages. It is also fully
    interoperable with Java.
  dependencies:
  - buildrequires:
      javapackages-tools:
      - 201801
      platform:
      - el8
      scala:
      - 2.1
    requires:
      platform: []
  components:
    rpms:
      hawtjni:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/hawtjni
        rationale: 'Runtime dependency of jansi, jansi-native.

          '
        ref: stream-scala-2.10
        repository: git://pkgs.devel.redhat.com/rpms/hawtjni
      jansi:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 30
        cache: http://pkgs.devel.redhat.com/repo/pkgs/jansi
        rationale: 'Runtime dependency of jline, scala.

          '
        ref: stream-scala-2.10
        repository: git://pkgs.devel.redhat.com/rpms/jansi
      jansi-native:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 20
        cache: http://pkgs.devel.redhat.com/repo/pkgs/jansi-native
        rationale: 'Runtime dependency of jansi.

          '
        ref: stream-scala-2.10
        repository: git://pkgs.devel.redhat.com/rpms/jansi-native
      jline:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 40
        cache: http://pkgs.devel.redhat.com/repo/pkgs/jline
        rationale: 'Runtime dependency of scala.

          '
        ref: stream-scala-2.10
        repository: git://pkgs.devel.redhat.com/rpms/jline
      scala:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 50
        cache: http://pkgs.devel.redhat.com/repo/pkgs/scala
        rationale: 'Module API.

          '
        ref: stream-scala-2.10
        repository: git://pkgs.devel.redhat.com/rpms/scala
  api:
    rpms:
    - scala
    - scala-apidoc
    - scala-swing
  buildopts:
    rpms:
      macros: '%_with_xmvn_javadoc 1

        %_without_asciidoc 1

        %_without_avalon 1

        %_without_bouncycastle 1

        %_without_cython 1

        %_without_dafsa 1

        %_without_desktop 1

        %_without_doxygen 1

        %_without_dtd 1

        %_without_eclipse 1

        %_without_ehcache 1

        %_without_emacs 1

        %_without_equinox 1

        %_without_fop 1

        %_without_ftp 1

        %_without_gradle 1

        %_without_groovy 1

        %_without_hadoop 1

        %_without_hsqldb 1

        %_without_itext 1

        %_without_jackson 1

        %_without_jmh 1

        %_without_jna 1

        %_without_jpa 1

        %_without_junit5 1

        %_without_logback 1

        %_without_markdown 1

        %_without_memcached 1

        %_without_memoryfilesystem 1

        %_without_obr 1

        %_without_python 1

        %_without_reporting 1

        %_without_scm 1

        %_without_snappy 1

        %_without_spring 1

        %_without_ssh 1

        %_without_testlib 1

        '
  profiles:
    common:
      rpms:
      - scala
  filter:
    rpms:
    - ant-scala
    - hawtjni
    - hawtjni-javadoc
    - jansi-javadoc
    - jansi-native-javadoc
    - jline-javadoc
    - maven-hawtjni-plugin
  artifacts:
    rpms:
    - hawtjni-0:1.16-1.module+el8+2477+516cbbff.noarch
    - hawtjni-javadoc-0:1.16-1.module+el8+2477+516cbbff.noarch
    - hawtjni-runtime-0:1.16-1.module+el8+2477+516cbbff.noarch
    - maven-hawtjni-plugin-0:1.16-1.module+el8+2477+516cbbff.noarch
    - jansi-native-0:1.7-5.module+el8+2477+516cbbff.x86_64
    - jansi-native-javadoc-0:1.7-5.module+el8+2477+516cbbff.noarch
    - jansi-0:1.17.1-1.module+el8+2477+516cbbff.noarch
    - jansi-javadoc-0:1.17.1-1.module+el8+2477+516cbbff.noarch
    - jline-0:2.14.6-2.module+el8+2477+516cbbff.noarch
    - jline-javadoc-0:2.14.6-2.module+el8+2477+516cbbff.noarch
    - scala-0:2.10.6-14.module+el8+2477+516cbbff.noarch
    - scala-apidoc-0:2.10.6-14.module+el8+2477+516cbbff.noarch
    - scala-swing-0:2.10.6-14.module+el8+2477+516cbbff.noarch
    - ant-scala-0:2.10.6-14.module+el8+2477+516cbbff.noarch
...
---
document: modulemd
version: 2
data:
  name: php
  stream: 7.3
  version: '8020020200715124551'
  context: ceb1cf90
  arch: x86_64
  license:
    content:
    - BSD
    - BSD and LGPLv3+
    - PHP
    - PHP and BSD
    - PHP and LGPLv2 and OpenLDAP
    - PHP and LGPLv2+
    - PHP and Zend and BSD and MIT and ASL 1.0 and NCSA
    - PHP and Zend and BSD and MIT and ASL 1.0 and NCSA and PostgreSQL
    module:
    - GPLv2+
  summary: PHP scripting language
  description: php 7.3 module
  dependencies:
  - buildrequires:
      httpd:
      - 2.4
      nginx:
      - 1.14
      platform:
      - el8
    requires:
      httpd:
      - 2.4
      nginx: []
      platform:
      - el8
  components:
    rpms:
      libzip:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: ZIP library
        ref: stream-php-7.3-rhel-8.2.0
      php:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: Module API.
        ref: stream-7.3-rhel-8.2.0
      php-pear:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 2
        rationale: Extension management
        ref: stream-php-7.3-rhel-8.2.0
      php-pecl-apcu:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 3
        rationale: APCu extension
        ref: stream-php-7.3-rhel-8.2.0
      php-pecl-rrd:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 3
        rationale: RRD extension
        ref: stream-php-7.3-rhel-8.2.0
      php-pecl-xdebug:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 3
        rationale: Xdebug extension
        ref: stream-php-7.3-rhel-8.2.0
      php-pecl-zip:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 3
        rationale: ZIP extension
        ref: stream-php-7.3-rhel-8.2.0
  api:
    rpms:
    - php-fpm
  references:
    documentation: http://php.net/
    tracker: https://bugs.php.net/
  profiles:
    common:
      rpms:
      - php-cli
      - php-common
      - php-fpm
      - php-json
      - php-mbstring
      - php-xml
    devel:
      rpms:
      - libzip
      - php-cli
      - php-common
      - php-devel
      - php-fpm
      - php-json
      - php-mbstring
      - php-pear
      - php-pecl-zip
      - php-process
      - php-xml
    minimal:
      rpms:
      - php-cli
      - php-common
  artifacts:
    rpms:
    - php-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-cli-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-dbg-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-fpm-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-common-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-devel-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-opcache-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-ldap-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pdo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-mysqlnd-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pgsql-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-process-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-odbc-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-soap-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-snmp-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-xml-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-xmlrpc-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-mbstring-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-gd-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-bcmath-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-gmp-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-dba-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-embedded-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-recode-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-intl-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-enchant-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-json-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-debugsource-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-cli-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-dbg-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-fpm-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-common-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-opcache-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-ldap-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pdo-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-mysqlnd-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pgsql-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-process-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-odbc-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-soap-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-snmp-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-xml-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-xmlrpc-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-mbstring-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-gd-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-bcmath-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-gmp-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-dba-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-embedded-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-recode-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-intl-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-enchant-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-json-debuginfo-0:7.3.20-1.module+el8.2.0+7373+b272fdef.x86_64
    - libzip-0:1.5.2-1.module+el8.2.0+7373+b272fdef.x86_64
    - libzip-devel-0:1.5.2-1.module+el8.2.0+7373+b272fdef.x86_64
    - libzip-tools-0:1.5.2-1.module+el8.2.0+7373+b272fdef.x86_64
    - libzip-debugsource-0:1.5.2-1.module+el8.2.0+7373+b272fdef.x86_64
    - libzip-debuginfo-0:1.5.2-1.module+el8.2.0+7373+b272fdef.x86_64
    - libzip-tools-debuginfo-0:1.5.2-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pear-1:1.10.9-1.module+el8.2.0+7373+b272fdef.noarch
    - php-pecl-zip-0:1.15.4-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pecl-zip-debugsource-0:1.15.4-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pecl-zip-debuginfo-0:1.15.4-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pecl-xdebug-0:2.8.0-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pecl-xdebug-debugsource-0:2.8.0-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pecl-xdebug-debuginfo-0:2.8.0-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pecl-rrd-0:2.0.1-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pecl-rrd-debugsource-0:2.0.1-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pecl-rrd-debuginfo-0:2.0.1-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pecl-apcu-0:5.1.17-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pecl-apcu-devel-0:5.1.17-1.module+el8.2.0+7373+b272fdef.x86_64
    - apcu-panel-0:5.1.17-1.module+el8.2.0+7373+b272fdef.noarch
    - php-pecl-apcu-debugsource-0:5.1.17-1.module+el8.2.0+7373+b272fdef.x86_64
    - php-pecl-apcu-debuginfo-0:5.1.17-1.module+el8.2.0+7373+b272fdef.x86_64
...
---
document: modulemd
version: 2
data:
  name: ruby
  stream: '2.5'
  version: '8030020200624105530'
  context: 30b713e6
  arch: x86_64
  license:
    content:
    - (BSD or Ruby) and PostgreSQL
    - (Ruby or BSD) and (Ruby or BSD or Python) and (Ruby or BSD or LGPLv2+)
    - (Ruby or BSD) and Public Domain and MIT and CC0 and zlib and UCD
    - (Ruby or GPLv2) and UCD
    - ASL 2.0
    - GPLv2 and Ruby and MIT and OFL
    - MIT
    - Ruby or BSD
    - Ruby or MIT
    module:
    - MIT
  summary: An interpreter of object-oriented scripting language
  description: Ruby is the interpreted scripting language for quick and easy object-oriented
    programming.  It has many features to process text files and to do system management
    tasks (as in Perl).  It is simple, straight-forward, and extensible.
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      ruby:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 101
        multilib:
        - x86_64
        rationale: An interpreter of object-oriented scripting language
        ref: stream-ruby-2.5-rhel-8.3.0
      rubygem-abrt:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 102
        rationale: ABRT support for Ruby
        ref: stream-ruby-2.5-rhel-8.3.0
      rubygem-bson:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 102
        rationale: Ruby Implementation of the BSON specification
        ref: stream-ruby-2.5-rhel-8.3.0
      rubygem-bundler:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 102
        rationale: Library and utilities to manage a Ruby application's gem dependencies
        ref: stream-ruby-2.5-rhel-8.3.0
      rubygem-mongo:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 103
        rationale: Ruby driver for MongoDB
        ref: stream-ruby-2.5-rhel-8.3.0
      rubygem-mysql2:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 102
        rationale: A simple, fast Mysql library for Ruby, binding to libmysql
        ref: stream-ruby-2.5-rhel-8.3.0
      rubygem-pg:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 102
        rationale: A Ruby interface to the PostgreSQL RDBMS
        ref: stream-ruby-2.5-rhel-8.3.0
  api:
    rpms:
    - ruby
    - ruby-devel
    - ruby-irb
    - ruby-libs
    - rubygem-abrt
    - rubygem-bigdecimal
    - rubygem-bson
    - rubygem-bundler
    - rubygem-did_you_mean
    - rubygem-io-console
    - rubygem-json
    - rubygem-minitest
    - rubygem-mongo
    - rubygem-mysql2
    - rubygem-net-telnet
    - rubygem-openssl
    - rubygem-pg
    - rubygem-power_assert
    - rubygem-psych
    - rubygem-rake
    - rubygem-rdoc
    - rubygem-test-unit
    - rubygem-xmlrpc
    - rubygems
    - rubygems-devel
  buildopts:
    rpms:
      macros: '%_without_rubypick 1

        '
  references:
    community: http://ruby-lang.org/
    documentation: https://www.ruby-lang.org/en/documentation/
    tracker: https://bugs.ruby-lang.org/
  profiles:
    common:
      rpms:
      - ruby
  artifacts:
    rpms:
    - rubygem-bson-debugsource-0:4.3.0-2.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-mongo-doc-0:2.5.1-2.module+el8.3.0+7153+c6f6daa5.noarch
    - ruby-libs-debuginfo-0:2.5.5-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - ruby-debugsource-0:2.5.5-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-net-telnet-0:0.1.1-106.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-abrt-doc-0:0.3.0-4.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-pg-debugsource-0:1.0.0-2.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-did_you_mean-0:1.2.0-106.module+el8.3.0+7153+c6f6daa5.noarch
    - ruby-debuginfo-0:2.5.5-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-test-unit-0:3.2.7-106.module+el8.3.0+7153+c6f6daa5.noarch
    - ruby-libs-0:2.5.5-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-bundler-0:1.16.1-3.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-rake-0:12.3.0-106.module+el8.3.0+7153+c6f6daa5.noarch
    - ruby-devel-0:2.5.5-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-mongo-0:2.5.1-2.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-bigdecimal-debuginfo-0:1.3.4-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - ruby-irb-0:2.5.5-106.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-mysql2-doc-0:0.4.10-4.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-bson-doc-0:4.3.0-2.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygems-0:2.7.6.2-106.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-bundler-doc-0:1.16.1-3.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-psych-debuginfo-0:3.0.2-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - ruby-doc-0:2.5.5-106.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-mysql2-debuginfo-0:0.4.10-4.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-mysql2-debugsource-0:0.4.10-4.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-pg-doc-0:1.0.0-2.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-json-0:2.1.0-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-json-debuginfo-0:2.1.0-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-io-console-debuginfo-0:0.4.6-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-mysql2-0:0.4.10-4.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-pg-0:1.0.0-2.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-minitest-0:5.10.3-106.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-rdoc-0:6.0.1-106.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-pg-debuginfo-0:1.0.0-2.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygems-devel-0:2.7.6.2-106.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-power_assert-0:1.1.1-106.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-bson-0:4.3.0-2.module+el8.3.0+7153+c6f6daa5.x86_64
    - ruby-0:2.5.5-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-bigdecimal-0:1.3.4-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-io-console-0:0.4.6-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-openssl-0:2.1.2-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-xmlrpc-0:0.3.0-106.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-psych-0:3.0.2-106.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-bson-debuginfo-0:4.3.0-2.module+el8.3.0+7153+c6f6daa5.x86_64
    - rubygem-abrt-0:0.3.0-4.module+el8.3.0+7153+c6f6daa5.noarch
    - rubygem-openssl-debuginfo-0:2.1.2-106.module+el8.3.0+7153+c6f6daa5.x86_64
...
---
document: modulemd
version: 2
data:
  name: nodejs
  stream: '14'
  version: '8030020201102105049'
  context: 229f0a1c
  arch: x86_64
  license:
    content:
    - MIT
    - MIT and ASL 2.0 and ISC and BSD
    module:
    - MIT
  summary: Javascript runtime
  description: Node.js is a platform built on Chrome's JavaScript runtime for easily
    building fast, scalable network applications. Node.js uses an event-driven, non-blocking
    I/O model that makes it lightweight and efficient, perfect for data-intensive
    real-time applications that run across distributed devices.
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      nodejs:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 100
        rationale: Javascript runtime and npm package manager.
        ref: stream-14-rhel-8.3.0
      nodejs-nodemon:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 200
        rationale: Simple monitor script for use during development of a node.js app
        ref: stream-14-rhel-8.3.0
      nodejs-packaging:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        rationale: RPM Macros and Utilities for Node.js Packaging
        ref: stream-14-rhel-8.3.0
  api:
    rpms:
    - nodejs
    - nodejs-devel
    - npm
  buildopts:
    rpms:
      macros: '%_with_bootstrap 1

        '
  references:
    community: http://nodejs.org
    documentation: http://nodejs.org/en/docs
    tracker: https://github.com/nodejs/node/issues
  profiles:
    common:
      rpms:
      - nodejs
      - npm
    development:
      rpms:
      - nodejs
      - nodejs-devel
      - npm
    minimal:
      rpms:
      - nodejs
    s2i:
      rpms:
      - nodejs
      - nodejs-nodemon
      - npm
  artifacts:
    rpms:
    - nodejs-packaging-0:23-3.module+el8.3.0+8610+0cf59502.noarch
    - nodejs-1:14.15.0-1.module+el8.3.0+8610+0cf59502.x86_64
    - nodejs-devel-1:14.15.0-1.module+el8.3.0+8610+0cf59502.x86_64
    - nodejs-full-i18n-1:14.15.0-1.module+el8.3.0+8610+0cf59502.x86_64
    - npm-1:6.14.8-1.14.15.0.1.module+el8.3.0+8610+0cf59502.x86_64
    - nodejs-docs-1:14.15.0-1.module+el8.3.0+8610+0cf59502.noarch
    - nodejs-debugsource-1:14.15.0-1.module+el8.3.0+8610+0cf59502.x86_64
    - nodejs-debuginfo-1:14.15.0-1.module+el8.3.0+8610+0cf59502.x86_64
    - nodejs-nodemon-0:2.0.3-1.module+el8.3.0+8610+0cf59502.noarch
...
---
document: modulemd
version: 2
data:
  name: php
  stream: '7.2'
  version: '8020020191108065827'
  context: 2c7ca891
  arch: x86_64
  license:
    content:
    - BSD
    - BSD and LGPLv3+
    - PHP
    - PHP and BSD
    - PHP and LGPLv2 and OpenLDAP
    - PHP and LGPLv2+
    - PHP and Zend and BSD and MIT and ASL 1.0
    module:
    - GPLv2+
  summary: PHP scripting language
  description: php 7.2 module
  dependencies:
  - buildrequires:
      httpd:
      - 2.4
      nginx:
      - 1.14
      platform:
      - el8.2.0
    requires:
      httpd:
      - 2.4
      nginx: []
      platform:
      - el8
  components:
    rpms:
      libzip:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: ZIP library
        ref: stream-php-7.2-rhel-8.2.0
      php:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: Module API.
        ref: stream-7.2-rhel-8.2.0
      php-pear:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 2
        rationale: Extension management
        ref: stream-php-7.2-rhel-8.2.0
      php-pecl-apcu:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 3
        rationale: APCu extension
        ref: stream-php-7.2-rhel-8.2.0
      php-pecl-zip:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 3
        rationale: ZIP extension
        ref: stream-php-7.2-rhel-8.2.0
  api:
    rpms:
    - php-fpm
  references:
    documentation: http://php.net/
    tracker: https://bugs.php.net/
  profiles:
    common:
      rpms:
      - php-cli
      - php-common
      - php-fpm
      - php-json
      - php-mbstring
      - php-xml
    devel:
      rpms:
      - libzip
      - php-cli
      - php-common
      - php-devel
      - php-fpm
      - php-json
      - php-mbstring
      - php-pear
      - php-pecl-zip
      - php-process
      - php-xml
    minimal:
      rpms:
      - php-cli
      - php-common
  artifacts:
    rpms:
    - php-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-cli-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-dbg-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-fpm-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-common-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-devel-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-opcache-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-ldap-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-pdo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-mysqlnd-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-pgsql-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-process-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-odbc-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-soap-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-snmp-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-xml-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-xmlrpc-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-mbstring-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-gd-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-bcmath-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-gmp-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-dba-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-embedded-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-recode-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-intl-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-enchant-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-json-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-debugsource-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-cli-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-dbg-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-fpm-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-common-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-opcache-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-ldap-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-pdo-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-mysqlnd-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-pgsql-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-process-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-odbc-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-soap-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-snmp-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-xml-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-xmlrpc-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-mbstring-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-gd-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-bcmath-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-gmp-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-dba-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-embedded-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-recode-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-intl-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-enchant-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-json-debuginfo-0:7.2.24-1.module+el8.2.0+4601+7c76a223.x86_64
    - libzip-0:1.5.1-2.module+el8.2.0+4601+7c76a223.x86_64
    - libzip-devel-0:1.5.1-2.module+el8.2.0+4601+7c76a223.x86_64
    - libzip-tools-0:1.5.1-2.module+el8.2.0+4601+7c76a223.x86_64
    - libzip-debugsource-0:1.5.1-2.module+el8.2.0+4601+7c76a223.x86_64
    - libzip-debuginfo-0:1.5.1-2.module+el8.2.0+4601+7c76a223.x86_64
    - libzip-tools-debuginfo-0:1.5.1-2.module+el8.2.0+4601+7c76a223.x86_64
    - php-pear-1:1.10.5-9.module+el8.2.0+4601+7c76a223.noarch
    - php-pecl-zip-0:1.15.3-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-pecl-zip-debugsource-0:1.15.3-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-pecl-zip-debuginfo-0:1.15.3-1.module+el8.2.0+4601+7c76a223.x86_64
    - php-pecl-apcu-0:5.1.12-2.module+el8.2.0+4601+7c76a223.x86_64
    - php-pecl-apcu-devel-0:5.1.12-2.module+el8.2.0+4601+7c76a223.x86_64
    - apcu-panel-0:5.1.12-2.module+el8.2.0+4601+7c76a223.noarch
    - php-pecl-apcu-debugsource-0:5.1.12-2.module+el8.2.0+4601+7c76a223.x86_64
    - php-pecl-apcu-debuginfo-0:5.1.12-2.module+el8.2.0+4601+7c76a223.x86_64
...
---
document: modulemd
version: 2
data:
  name: mysql
  stream: '8.0'
  version: '8020020200828111438'
  context: 4cda2c84
  arch: x86_64
  license:
    content:
    - BSD or LGPLv2+ or GPL+
    - GPLv2 with exceptions and LGPLv2 and BSD
    - mecab-ipadic
    module:
    - MIT
  summary: MySQL Module
  description: MySQL is a multi-user, multi-threaded SQL database server. MySQL is
    a client/server implementation consisting of a server daemon (mysqld) and many
    different client programs and libraries. The base package contains the standard
    MySQL client programs and generic MySQL files.
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  api:
    rpms:
    - mysql
    - mysql-server
  components:
    rpms:
      mecab:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 8
        rationale: A dependency of mysql
        ref: stream-8.0-rhel-8.2.0
      mecab-ipadic:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 9
        rationale: A dictionary for mecab
        ref: stream-8.0-rhel-8.2.0
      mysql:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        rationale: MySQL server package
        ref: stream-8.0-rhel-8.2.0
      rapidjson:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 7
        rationale: A build-time only dependency of mysql
        ref: dbf36eb90
  buildopts:
    rpms:
      macros: '%runselftest 1

        %check_testsuite 1

        '
  references:
    community: https://dev.mysql.com/
    documentation: https://dev.mysql.com/doc/refman/8.0/en/
    tracker: http://bugzilla.redhat.com/
  profiles:
    client:
      rpms:
      - mysql
    server:
      rpms:
      - mysql-server
  filter:
    rpms:
    - mecab-devel
    - rapidjson
    - rapidjson-devel
    - rapidjson-doc
  artifacts:
    rpms:
    - mysql-debugsource-0:8.0.21-1.module+el8.2.0+7855+47abd494.x86_64
    - mysql-libs-0:8.0.21-1.module+el8.2.0+7855+47abd494.x86_64
    - mysql-devel-debuginfo-0:8.0.21-1.module+el8.2.0+7855+47abd494.x86_64
    - mysql-0:8.0.21-1.module+el8.2.0+7855+47abd494.x86_64
    - mecab-debugsource-0:0.996-1.module+el8.2.0+7855+47abd494.9.x86_64
    - mecab-ipadic-0:2.7.0.20070801-16.module+el8.2.0+7855+47abd494.x86_64
    - mysql-common-0:8.0.21-1.module+el8.2.0+7855+47abd494.x86_64
    - mysql-devel-0:8.0.21-1.module+el8.2.0+7855+47abd494.x86_64
    - rapidjson-doc-0:1.1.0-3.module+el8.2.0+7855+47abd494.noarch
    - rapidjson-devel-0:1.1.0-3.module+el8.2.0+7855+47abd494.noarch
    - mecab-0:0.996-1.module+el8.2.0+7855+47abd494.9.x86_64
    - mysql-debuginfo-0:8.0.21-1.module+el8.2.0+7855+47abd494.x86_64
    - mecab-devel-0:0.996-1.module+el8.2.0+7855+47abd494.9.x86_64
    - mecab-ipadic-EUCJP-0:2.7.0.20070801-16.module+el8.2.0+7855+47abd494.x86_64
    - mysql-server-debuginfo-0:8.0.21-1.module+el8.2.0+7855+47abd494.x86_64
    - mysql-libs-debuginfo-0:8.0.21-1.module+el8.2.0+7855+47abd494.x86_64
    - mysql-server-0:8.0.21-1.module+el8.2.0+7855+47abd494.x86_64
    - mysql-test-debuginfo-0:8.0.21-1.module+el8.2.0+7855+47abd494.x86_64
    - mysql-test-0:8.0.21-1.module+el8.2.0+7855+47abd494.x86_64
    - mecab-debuginfo-0:0.996-1.module+el8.2.0+7855+47abd494.9.x86_64
    - mysql-errmsg-0:8.0.21-1.module+el8.2.0+7855+47abd494.x86_64
...
---
document: modulemd
version: 2
data:
  name: nodejs
  stream: '12'
  version: '8030020201124152102'
  context: 229f0a1c
  arch: x86_64
  license:
    content:
    - MIT
    - MIT and ASL 2.0 and ISC and BSD
    module:
    - MIT
  summary: Javascript runtime
  description: Node.js is a platform built on Chrome's JavaScript runtime for easily
    building fast, scalable network applications. Node.js uses an event-driven, non-blocking
    I/O model that makes it lightweight and efficient, perfect for data-intensive
    real-time applications that run across distributed devices.
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      nodejs:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 100
        rationale: Javascript runtime and npm package manager.
        ref: stream-12-rhel-8.3.0
      nodejs-nodemon:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 200
        rationale: Simple monitor script for use during development of a node.js app
        ref: stream-12-rhel-8.3.0
      nodejs-packaging:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        rationale: RPM Macros and Utilities for Node.js Packaging
        ref: stream-12-rhel-8.3.0
  api:
    rpms:
    - nodejs
    - nodejs-devel
    - npm
  buildopts:
    rpms:
      macros: '%_with_bootstrap 1

        %_with_shared_brotli 1

        '
  references:
    community: http://nodejs.org
    documentation: http://nodejs.org/en/docs
    tracker: https://github.com/nodejs/node/issues
  profiles:
    common:
      rpms:
      - nodejs
      - npm
    development:
      rpms:
      - nodejs
      - nodejs-devel
      - npm
    minimal:
      rpms:
      - nodejs
    s2i:
      rpms:
      - nodejs
      - nodejs-nodemon
      - npm
  artifacts:
    rpms:
    - nodejs-packaging-0:17-3.module+el8.3.0+8851+b7b41ca0.noarch
    - nodejs-1:12.19.1-1.module+el8.3.0+8851+b7b41ca0.x86_64
    - nodejs-devel-1:12.19.1-1.module+el8.3.0+8851+b7b41ca0.x86_64
    - nodejs-full-i18n-1:12.19.1-1.module+el8.3.0+8851+b7b41ca0.x86_64
    - npm-1:6.14.8-1.12.19.1.1.module+el8.3.0+8851+b7b41ca0.x86_64
    - nodejs-docs-1:12.19.1-1.module+el8.3.0+8851+b7b41ca0.noarch
    - nodejs-debugsource-1:12.19.1-1.module+el8.3.0+8851+b7b41ca0.x86_64
    - nodejs-debuginfo-1:12.19.1-1.module+el8.3.0+8851+b7b41ca0.x86_64
    - nodejs-nodemon-0:1.18.3-1.module+el8.3.0+8851+b7b41ca0.noarch
...
---
document: modulemd
version: 2
data:
  name: redis
  stream: '5'
  version: '8000020190711140130'
  context: f8e95b4e
  arch: x86_64
  license:
    content:
    - BSD and MIT
    - CC-BY-SA
    module:
    - GPLv2+
  summary: Redis persistent key-value database
  description: redis 5 module
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      redis:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: Module API.
        ref: stream-5.0-rhel-8.0.0
  api:
    rpms:
    - redis
  buildopts:
    rpms:
      macros: '%_without_redistrib 1

        '
  references:
    documentation: https://redis.io/documentation
    tracker: https://github.com/antirez/redis/issues
  profiles:
    common:
      rpms:
      - redis
  artifacts:
    rpms:
    - redis-0:5.0.3-2.module+el8.0.0.z+3657+acb471dc.x86_64
    - redis-devel-0:5.0.3-2.module+el8.0.0.z+3657+acb471dc.x86_64
    - redis-doc-0:5.0.3-2.module+el8.0.0.z+3657+acb471dc.noarch
    - redis-debugsource-0:5.0.3-2.module+el8.0.0.z+3657+acb471dc.x86_64
    - redis-debuginfo-0:5.0.3-2.module+el8.0.0.z+3657+acb471dc.x86_64
...
---
document: modulemd
version: 2
data:
  name: parfait
  stream: '0.5'
  version: '820181213142511'
  context: d2b614b2
  arch: x86_64
  license:
    content:
    - ASL 2.0
    - BSD
    module:
    - ASL 2.0
  summary: Parfait Module
  description: Parfait is a Java performance monitoring library that exposes and collects
    metrics through a variety of outputs.  It provides APIs for extracting performance
    metrics from the JVM and other sources. It interfaces to Performance Co-Pilot
    (PCP) using the Memory Mapped Value (MMV) machinery for extremely lightweight
    instrumentation.
  dependencies:
  - buildrequires:
      javapackages-tools:
      - 201801
      pki-deps:
      - 10.6
      platform:
      - el8
    requires:
      javapackages-runtime:
      - 201801
      pki-deps:
      - 10.6
      platform:
      - el8
  components:
    rpms:
      log4j12:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 80
        cache: http://pkgs.devel.redhat.com/repo/pkgs/log4j12
        rationale: Needed as a runtime dep for parfait.
        ref: stream-javapackages-tools-201801
        repository: git://pkgs.devel.redhat.com/rpms/log4j12
      parfait:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 70
        cache: http://pkgs.devel.redhat.com/repo/pkgs/parfait
        rationale: Main Parfait Package
        ref: stream-0.5
        repository: git://pkgs.devel.redhat.com/rpms/parfait
      si-units:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 50
        cache: http://pkgs.devel.redhat.com/repo/pkgs/si-units
        rationale: A library of SI quantities and unit types (JSR 363).
        ref: stream-0.5
        repository: git://pkgs.devel.redhat.com/rpms/si-units
      unit-api:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/unit-api
        rationale: "The Unit of Measurement library provides a set of Java language\
          \ programming interfaces for handling units and quantities. The interfaces\
          \ provide a layer which separates client code, which would call the API,\
          \ from library code, which implements the API.\nThe specification contains\
          \ Interfaces and abstract classes with methods for unit operations:\n\n\
          \  * Checking of unit compatibility\n  * Expression of a quantity in various\
          \ units\n  * Arithmetic operations on units"
        ref: stream-0.5
        repository: git://pkgs.devel.redhat.com/rpms/unit-api
      uom-lib:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 30
        cache: http://pkgs.devel.redhat.com/repo/pkgs/uom-lib
        rationale: Units of Measurement Libraries - extending and complementing JSR
          363.
        ref: stream-0.5
        repository: git://pkgs.devel.redhat.com/rpms/uom-lib
      uom-parent:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 20
        cache: http://pkgs.devel.redhat.com/repo/pkgs/uom-parent
        rationale: Main parent POM for all Units of Measurement Maven projects.
        ref: stream-0.5
        repository: git://pkgs.devel.redhat.com/rpms/uom-parent
      uom-se:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 40
        cache: http://pkgs.devel.redhat.com/repo/pkgs/uom-se
        rationale: This package contains documentation for the Units Standard (JSR
          363) Java SE 8 Implementation.
        ref: stream-0.5
        repository: git://pkgs.devel.redhat.com/rpms/uom-se
      uom-systems:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 60
        cache: http://pkgs.devel.redhat.com/repo/pkgs/uom-systems
        rationale: Units of Measurement Systems - modules for JSR 363.
        ref: stream-0.5
        repository: git://pkgs.devel.redhat.com/rpms/uom-systems
  api:
    rpms:
    - parfait
    - parfait-examples
    - pcp-parfait-agent
  profiles:
    common:
      rpms:
      - parfait
      - parfait-examples
      - pcp-parfait-agent
  artifacts:
    rpms:
    - unit-api-0:1.0-5.module+el8+2463+615f6896.noarch
    - unit-api-javadoc-0:1.0-5.module+el8+2463+615f6896.noarch
    - uom-parent-0:1.0.3-3.module+el8+2463+615f6896.noarch
    - uom-lib-0:1.0.1-6.module+el8+2463+615f6896.noarch
    - uom-lib-javadoc-0:1.0.1-6.module+el8+2463+615f6896.noarch
    - uom-se-0:1.0.4-3.module+el8+2463+615f6896.noarch
    - uom-se-javadoc-0:1.0.4-3.module+el8+2463+615f6896.noarch
    - si-units-0:0.6.5-2.module+el8+2463+615f6896.noarch
    - si-units-javadoc-0:0.6.5-2.module+el8+2463+615f6896.noarch
    - uom-systems-0:0.7-1.module+el8+2463+615f6896.noarch
    - uom-systems-javadoc-0:0.7-1.module+el8+2463+615f6896.noarch
    - parfait-0:0.5.4-2.module+el8+2463+615f6896.noarch
    - parfait-javadoc-0:0.5.4-2.module+el8+2463+615f6896.noarch
    - pcp-parfait-agent-0:0.5.4-2.module+el8+2463+615f6896.noarch
    - parfait-examples-0:0.5.4-2.module+el8+2463+615f6896.noarch
    - log4j12-0:1.2.17-22.module+el8+2463+615f6896.noarch
    - log4j12-javadoc-0:1.2.17-22.module+el8+2463+615f6896.noarch
...
---
document: modulemd
version: 2
data:
  name: nodejs
  stream: '10'
  version: '8020020200617141353'
  context: 4cda2c84
  arch: x86_64
  license:
    content:
    - MIT
    - MIT and ASL 2.0 and ISC and BSD
    module:
    - MIT
  summary: Javascript runtime
  description: Node.js is a platform built on Chrome's JavaScript runtime for easily
    building fast, scalable network applications. Node.js uses an event-driven, non-blocking
    I/O model that makes it lightweight and efficient, perfect for data-intensive
    real-time applications that run across distributed devices.
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      nodejs:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        rationale: Javascript runtime and npm package manager.
        ref: stream-10-rhel-8.2.0
      nodejs-nodemon:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 200
        rationale: Simple monitor script for use during development of a node.js app
        ref: stream-rhel-8.0-rhel-8.2.0
      nodejs-packaging:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 100
        rationale: RPM Macros and Utilities for Node.js Packaging
        ref: stream-rhel-8.0-rhel-8.2.0
  api:
    rpms:
    - nodejs
    - nodejs-devel
    - npm
  buildopts:
    rpms:
      macros: '%_with_bootstrap 1

        '
  references:
    community: http://nodejs.org
    documentation: http://nodejs.org/en/docs
    tracker: https://github.com/nodejs/node/issues
  profiles:
    common:
      rpms:
      - nodejs
      - npm
    development:
      rpms:
      - nodejs
      - nodejs-devel
      - npm
    minimal:
      rpms:
      - nodejs
    s2i:
      rpms:
      - nodejs
      - nodejs-nodemon
      - npm
  artifacts:
    rpms:
    - nodejs-1:10.21.0-3.module+el8.2.0+7071+d2377ea3.x86_64
    - nodejs-devel-1:10.21.0-3.module+el8.2.0+7071+d2377ea3.x86_64
    - nodejs-full-i18n-1:10.21.0-3.module+el8.2.0+7071+d2377ea3.x86_64
    - npm-1:6.14.4-1.10.21.0.3.module+el8.2.0+7071+d2377ea3.x86_64
    - nodejs-docs-1:10.21.0-3.module+el8.2.0+7071+d2377ea3.noarch
    - nodejs-debugsource-1:10.21.0-3.module+el8.2.0+7071+d2377ea3.x86_64
    - nodejs-debuginfo-1:10.21.0-3.module+el8.2.0+7071+d2377ea3.x86_64
    - nodejs-packaging-0:17-3.module+el8.2.0+7071+d2377ea3.noarch
    - nodejs-nodemon-0:1.18.3-1.module+el8.2.0+7071+d2377ea3.noarch
...
---
document: modulemd
version: 2
data:
  name: nginx
  stream: '1.18'
  version: '8030020200529144723'
  context: 30b713e6
  arch: x86_64
  license:
    content:
    - BSD
    module:
    - MIT
  summary: nginx webserver
  description: nginx 1.18 webserver module
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      nginx:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Module API.
        ref: stream-1.18-rhel-8.3.0
  api:
    rpms:
    - nginx
    - nginx-all-modules
    - nginx-filesystem
    - nginx-mod-http-image-filter
    - nginx-mod-http-perl
    - nginx-mod-http-xslt-filter
    - nginx-mod-mail
    - nginx-mod-stream
  references:
    documentation: http://nginx.org/en/docs/
    tracker: https://trac.nginx.org/nginx/
  profiles:
    common:
      rpms:
      - nginx
      - nginx-all-modules
      - nginx-filesystem
      - nginx-mod-http-image-filter
      - nginx-mod-http-perl
      - nginx-mod-http-xslt-filter
      - nginx-mod-mail
      - nginx-mod-stream
  artifacts:
    rpms:
    - nginx-1:1.18.0-2.module+el8.3.0+6830+4321f41c.x86_64
    - nginx-all-modules-1:1.18.0-2.module+el8.3.0+6830+4321f41c.noarch
    - nginx-filesystem-1:1.18.0-2.module+el8.3.0+6830+4321f41c.noarch
    - nginx-mod-http-image-filter-1:1.18.0-2.module+el8.3.0+6830+4321f41c.x86_64
    - nginx-mod-http-perl-1:1.18.0-2.module+el8.3.0+6830+4321f41c.x86_64
    - nginx-mod-http-xslt-filter-1:1.18.0-2.module+el8.3.0+6830+4321f41c.x86_64
    - nginx-mod-mail-1:1.18.0-2.module+el8.3.0+6830+4321f41c.x86_64
    - nginx-mod-stream-1:1.18.0-2.module+el8.3.0+6830+4321f41c.x86_64
    - nginx-debugsource-1:1.18.0-2.module+el8.3.0+6830+4321f41c.x86_64
    - nginx-debuginfo-1:1.18.0-2.module+el8.3.0+6830+4321f41c.x86_64
    - nginx-mod-http-image-filter-debuginfo-1:1.18.0-2.module+el8.3.0+6830+4321f41c.x86_64
    - nginx-mod-http-perl-debuginfo-1:1.18.0-2.module+el8.3.0+6830+4321f41c.x86_64
    - nginx-mod-http-xslt-filter-debuginfo-1:1.18.0-2.module+el8.3.0+6830+4321f41c.x86_64
    - nginx-mod-mail-debuginfo-1:1.18.0-2.module+el8.3.0+6830+4321f41c.x86_64
    - nginx-mod-stream-debuginfo-1:1.18.0-2.module+el8.3.0+6830+4321f41c.x86_64
...
---
document: modulemd
version: 2
data:
  name: nginx
  stream: '1.16'
  version: '8030020201124104955'
  context: 229f0a1c
  arch: x86_64
  license:
    content:
    - BSD
    module:
    - MIT
  summary: nginx webserver
  description: nginx 1.16 webserver module
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      nginx:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Module API.
        ref: stream-1.16-rhel-8.3.0
  api:
    rpms:
    - nginx
    - nginx-all-modules
    - nginx-filesystem
    - nginx-mod-http-image-filter
    - nginx-mod-http-perl
    - nginx-mod-http-xslt-filter
    - nginx-mod-mail
    - nginx-mod-stream
  references:
    documentation: http://nginx.org/en/docs/
    tracker: https://trac.nginx.org/nginx/
  profiles:
    common:
      rpms:
      - nginx
      - nginx-all-modules
      - nginx-filesystem
      - nginx-mod-http-image-filter
      - nginx-mod-http-perl
      - nginx-mod-http-xslt-filter
      - nginx-mod-mail
      - nginx-mod-stream
  artifacts:
    rpms:
    - nginx-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.x86_64
    - nginx-all-modules-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.noarch
    - nginx-filesystem-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.noarch
    - nginx-mod-http-image-filter-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.x86_64
    - nginx-mod-http-perl-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.x86_64
    - nginx-mod-http-xslt-filter-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.x86_64
    - nginx-mod-mail-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.x86_64
    - nginx-mod-stream-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.x86_64
    - nginx-debugsource-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.x86_64
    - nginx-debuginfo-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.x86_64
    - nginx-mod-http-image-filter-debuginfo-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.x86_64
    - nginx-mod-http-perl-debuginfo-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.x86_64
    - nginx-mod-http-xslt-filter-debuginfo-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.x86_64
    - nginx-mod-mail-debuginfo-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.x86_64
    - nginx-mod-stream-debuginfo-1:1.16.1-1.module+el8.3.0+8844+e5e7039f.1.1.x86_64
...
---
document: modulemd
version: 2
data:
  name: nginx
  stream: '1.14'
  version: '8000020190830002848'
  context: f8e95b4e
  arch: x86_64
  license:
    content:
    - BSD
    module:
    - MIT
  summary: nginx webserver
  description: nginx 1.14 webserver module
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      nginx:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Module API.
        ref: stream-1.14-rhel-8.0.0
  api:
    rpms:
    - nginx
    - nginx-all-modules
    - nginx-filesystem
    - nginx-mod-http-image-filter
    - nginx-mod-http-perl
    - nginx-mod-http-xslt-filter
    - nginx-mod-mail
    - nginx-mod-stream
  references:
    documentation: http://nginx.org/en/docs/
    tracker: https://trac.nginx.org/nginx/
  profiles:
    common:
      rpms:
      - nginx
      - nginx-all-modules
      - nginx-filesystem
      - nginx-mod-http-image-filter
      - nginx-mod-http-perl
      - nginx-mod-http-xslt-filter
      - nginx-mod-mail
      - nginx-mod-stream
  artifacts:
    rpms:
    - nginx-1:1.14.1-9.module+el8.0.0+4108+af250afe.x86_64
    - nginx-all-modules-1:1.14.1-9.module+el8.0.0+4108+af250afe.noarch
    - nginx-filesystem-1:1.14.1-9.module+el8.0.0+4108+af250afe.noarch
    - nginx-mod-http-image-filter-1:1.14.1-9.module+el8.0.0+4108+af250afe.x86_64
    - nginx-mod-http-perl-1:1.14.1-9.module+el8.0.0+4108+af250afe.x86_64
    - nginx-mod-http-xslt-filter-1:1.14.1-9.module+el8.0.0+4108+af250afe.x86_64
    - nginx-mod-mail-1:1.14.1-9.module+el8.0.0+4108+af250afe.x86_64
    - nginx-mod-stream-1:1.14.1-9.module+el8.0.0+4108+af250afe.x86_64
    - nginx-debugsource-1:1.14.1-9.module+el8.0.0+4108+af250afe.x86_64
    - nginx-debuginfo-1:1.14.1-9.module+el8.0.0+4108+af250afe.x86_64
    - nginx-mod-http-image-filter-debuginfo-1:1.14.1-9.module+el8.0.0+4108+af250afe.x86_64
    - nginx-mod-http-perl-debuginfo-1:1.14.1-9.module+el8.0.0+4108+af250afe.x86_64
    - nginx-mod-http-xslt-filter-debuginfo-1:1.14.1-9.module+el8.0.0+4108+af250afe.x86_64
    - nginx-mod-mail-debuginfo-1:1.14.1-9.module+el8.0.0+4108+af250afe.x86_64
    - nginx-mod-stream-debuginfo-1:1.14.1-9.module+el8.0.0+4108+af250afe.x86_64
...
---
document: modulemd
version: 2
data:
  name: mod_auth_openidc
  stream: '2.3'
  version: '8020020200604180605'
  context: 4cda2c84
  arch: x86_64
  license:
    content:
    - ASL 2.0
    - MIT
    module:
    - MIT
  summary: Apache module suporting OpenID Connect authentication
  description: This module enables an Apache 2.x web server to operate as an OpenID
    Connect Relying Party and/or OAuth 2.0 Resource Server.
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  components:
    rpms:
      cjose:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: Provides JOSE support
        ref: stream-mod_auth_open_idc-2.3-rhel-8.2.0
      mod_auth_openidc:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 2
        rationale: Provides the core functionality.
        ref: stream-mod_auth_open_idc-2.3-rhel-8.2.0
  references:
    community: https://github.com/zmartzone/mod_auth_openidc
    documentation: https://github.com/zmartzone/mod_auth_openidc/wiki
    tracker: https://github.com/zmartzone/mod_auth_openidc/issues
  artifacts:
    rpms:
    - cjose-0:0.6.1-2.module+el8.2.0+6919+ac02cfd2.3.x86_64
    - cjose-devel-0:0.6.1-2.module+el8.2.0+6919+ac02cfd2.3.x86_64
    - cjose-debugsource-0:0.6.1-2.module+el8.2.0+6919+ac02cfd2.3.x86_64
    - cjose-debuginfo-0:0.6.1-2.module+el8.2.0+6919+ac02cfd2.3.x86_64
    - mod_auth_openidc-0:2.3.7-4.module+el8.2.0+6919+ac02cfd2.3.3.x86_64
    - mod_auth_openidc-debugsource-0:2.3.7-4.module+el8.2.0+6919+ac02cfd2.3.3.x86_64
    - mod_auth_openidc-debuginfo-0:2.3.7-4.module+el8.2.0+6919+ac02cfd2.3.3.x86_64
...
---
document: modulemd
version: 2
data:
  name: mercurial
  stream: '4.8'
  version: '820190108205035'
  context: 77fc8825
  arch: x86_64
  license:
    content:
    - GPLv2+
    module:
    - MIT
  summary: Mercurial -- a distributed SCM
  description: Mercurial is a fast, lightweight source control management system designed
    for efficient handling of very large distributed projects.
  dependencies:
  - buildrequires:
      platform:
      - el8
      python27:
      - 2.7
    requires:
      platform:
      - el8
      python27:
      - 2.7
  api:
    rpms:
    - mercurial
    - mercurial-hgk
  components:
    rpms:
      mercurial:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        cache: http://pkgs.devel.redhat.com/repo/pkgs/mercurial
        rationale: Mercurial -- a distributed SCM
        ref: stream-mercurial-4.8
        repository: git://pkgs.devel.redhat.com/rpms/mercurial
  references:
    community: https://www.mercurial-scm.org/
    documentation: https://www.mercurial-scm.org/guide
    tracker: https://www.mercurial-scm.org/wiki/BugTracker
  profiles:
    common:
      rpms:
      - mercurial
  artifacts:
    rpms:
    - mercurial-hgk-0:4.8.2-1.module+el8+2647+365c7305.x86_64
    - mercurial-0:4.8.2-1.module+el8+2647+365c7305.x86_64
    - mercurial-debugsource-0:4.8.2-1.module+el8+2647+365c7305.x86_64
    - mercurial-debuginfo-0:4.8.2-1.module+el8+2647+365c7305.x86_64
...
---
document: modulemd
version: 2
data:
  name: maven
  stream: '3.5'
  version: '820181213140354'
  context: 5ea3b708
  arch: x86_64
  license:
    content:
    - (CDDL or GPLv2 with exceptions) and ASL 2.0
    - ASL 1.1 and ASL 2.0 and xpp and BSD and Public Domain
    - ASL 2.0
    - ASL 2.0 and ASL 1.1 and MIT
    - ASL 2.0 and CC0
    - ASL 2.0 and EPL-1.0 and BSD
    - ASL 2.0 and MIT
    - ASL 2.0 and MIT and xpp
    - ASL 2.0 and Plexus
    - CDDL or GPLv2 with exceptions
    - EPL-1.0 and BSD
    - MIT
    - MIT and ASL 2.0
    - Public Domain
    module:
    - MIT
  summary: Java project management and project comprehension tool
  description: Maven is a software project management and comprehension tool. Based
    on the concept of a project object model (POM), Maven can manage a project's build,
    reporting and documentation from a central piece of information.
  dependencies:
  - buildrequires:
      javapackages-tools:
      - 201801
      platform:
      - el8
    requires:
      platform: []
  api:
    rpms:
    - maven
  components:
    rpms:
      aopalliance:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/aopalliance
        rationale: 'Runtime dependency of google-guice, maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/aopalliance
      apache-commons-cli:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/apache-commons-cli
        rationale: 'Runtime dependency of maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/apache-commons-cli
      apache-commons-codec:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/apache-commons-codec
        rationale: 'Runtime dependency of httpcomponents-client, maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/apache-commons-codec
      apache-commons-io:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/apache-commons-io
        rationale: "Runtime dependency of maven, maven-shared-utils,\n     maven-wagon.\n"
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/apache-commons-io
      apache-commons-lang3:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/apache-commons-lang3
        rationale: 'Runtime dependency of maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/apache-commons-lang3
      apache-commons-logging:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/apache-commons-logging
        rationale: 'Runtime dependency of httpcomponents-client, maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/apache-commons-logging
      atinject:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/atinject
        rationale: 'Runtime dependency of cdi-api, google-guice, maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/atinject
      cdi-api:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 20
        cache: http://pkgs.devel.redhat.com/repo/pkgs/cdi-api
        rationale: 'Runtime dependency of maven, sisu.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/cdi-api
      geronimo-annotation:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/geronimo-annotation
        rationale: 'Runtime dependency of maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/geronimo-annotation
      glassfish-el:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/glassfish-el
        rationale: 'Runtime dependency of cdi-api.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/glassfish-el
      google-guice:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 20
        cache: http://pkgs.devel.redhat.com/repo/pkgs/google-guice
        rationale: 'Runtime dependency of maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/google-guice
      guava20:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/guava20
        rationale: 'Runtime dependency of google-guice, maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/guava20
      hawtjni:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/hawtjni
        rationale: 'Runtime dependency of jansi, jansi-native, maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/hawtjni
      httpcomponents-client:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 20
        cache: http://pkgs.devel.redhat.com/repo/pkgs/httpcomponents-client
        rationale: 'Runtime dependency of maven, maven-wagon.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/httpcomponents-client
      httpcomponents-core:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/httpcomponents-core
        rationale: "Runtime dependency of httpcomponents-client, maven,\n     maven-wagon.\n"
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/httpcomponents-core
      jansi:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 30
        cache: http://pkgs.devel.redhat.com/repo/pkgs/jansi
        rationale: 'Runtime dependency of maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/jansi
      jansi-native:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 20
        cache: http://pkgs.devel.redhat.com/repo/pkgs/jansi-native
        rationale: 'Runtime dependency of jansi, maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/jansi-native
      jboss-interceptors-1.2-api:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/jboss-interceptors-1.2-api
        rationale: 'Runtime dependency of cdi-api.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/jboss-interceptors-1.2-api
      jsoup:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/jsoup
        rationale: 'Runtime dependency of maven-wagon.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/jsoup
      maven:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 50
        cache: http://pkgs.devel.redhat.com/repo/pkgs/maven
        rationale: 'Module API.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/maven
      maven-resolver:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 40
        cache: http://pkgs.devel.redhat.com/repo/pkgs/maven-resolver
        rationale: 'Runtime dependency of maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/maven-resolver
      maven-shared-utils:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 20
        cache: http://pkgs.devel.redhat.com/repo/pkgs/maven-shared-utils
        rationale: 'Runtime dependency of maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/maven-shared-utils
      maven-wagon:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 30
        cache: http://pkgs.devel.redhat.com/repo/pkgs/maven-wagon
        rationale: 'Runtime dependency of maven, maven-resolver.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/maven-wagon
      plexus-cipher:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/plexus-cipher
        rationale: 'Runtime dependency of maven, plexus-sec-dispatcher.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/plexus-cipher
      plexus-classworlds:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/plexus-classworlds
        rationale: 'Runtime dependency of maven, sisu.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/plexus-classworlds
      plexus-containers:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/plexus-containers
        rationale: 'Runtime dependency of maven, sisu.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/plexus-containers
      plexus-interpolation:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/plexus-interpolation
        rationale: 'Runtime dependency of maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/plexus-interpolation
      plexus-sec-dispatcher:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 20
        cache: http://pkgs.devel.redhat.com/repo/pkgs/plexus-sec-dispatcher
        rationale: 'Runtime dependency of maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/plexus-sec-dispatcher
      plexus-utils:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/plexus-utils
        rationale: "Runtime dependency of maven, maven-wagon,\n     plexus-sec-dispatcher,\
          \ sisu.\n"
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/plexus-utils
      sisu:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 30
        cache: http://pkgs.devel.redhat.com/repo/pkgs/sisu
        rationale: 'Runtime dependency of maven.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/sisu
      slf4j:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/slf4j
        rationale: 'Runtime dependency of maven, maven-wagon.

          '
        ref: stream-maven-3.5
        repository: git://pkgs.devel.redhat.com/rpms/slf4j
  buildopts:
    rpms:
      macros: '%_with_xmvn_javadoc 1

        %_without_asciidoc 1

        %_without_avalon 1

        %_without_bouncycastle 1

        %_without_cython 1

        %_without_dafsa 1

        %_without_desktop 1

        %_without_dom4j 1

        %_without_doxygen 1

        %_without_dtd 1

        %_without_eclipse 1

        %_without_ehcache 1

        %_without_emacs 1

        %_without_equinox 1

        %_without_fop 1

        %_without_ftp 1

        %_without_gradle 1

        %_without_groovy 1

        %_without_hadoop 1

        %_without_hsqldb 1

        %_without_itext 1

        %_without_jackson 1

        %_without_jmh 1

        %_without_jna 1

        %_without_jpa 1

        %_without_junit5 1

        %_without_logback 1

        %_without_markdown 1

        %_without_memcached 1

        %_without_memoryfilesystem 1

        %_without_obr 1

        %_without_python 1

        %_without_reporting 1

        %_without_scm 1

        %_without_snakeyaml 1

        %_without_snappy 1

        %_without_spring 1

        %_without_ssh 1

        %_without_testlib 1

        %_without_vfs 1

        '
  profiles:
    common:
      rpms:
      - maven
  filter:
    rpms:
    - aopalliance-javadoc
    - apache-commons-cli-javadoc
    - apache-commons-codec-javadoc
    - apache-commons-io-javadoc
    - apache-commons-lang3-javadoc
    - apache-commons-logging-javadoc
    - atinject-javadoc
    - atinject-tck
    - cdi-api-javadoc
    - geronimo-annotation-javadoc
    - glassfish-el
    - glassfish-el-javadoc
    - google-guice-javadoc
    - guava20-javadoc
    - guava20-testlib
    - guice-assistedinject
    - guice-bom
    - guice-extensions
    - guice-grapher
    - guice-jmx
    - guice-jndi
    - guice-multibindings
    - guice-parent
    - guice-servlet
    - guice-testlib
    - guice-throwingproviders
    - hawtjni
    - hawtjni-javadoc
    - httpcomponents-client-cache
    - httpcomponents-client-javadoc
    - httpcomponents-core-javadoc
    - jansi-javadoc
    - jansi-native-javadoc
    - jboss-interceptors-1.2-api-javadoc
    - jsoup-javadoc
    - jul-to-slf4j
    - log4j-over-slf4j
    - maven-hawtjni-plugin
    - maven-javadoc
    - maven-resolver
    - maven-resolver-javadoc
    - maven-resolver-test-util
    - maven-resolver-transport-classpath
    - maven-resolver-transport-file
    - maven-resolver-transport-http
    - maven-shared-utils-javadoc
    - maven-wagon
    - maven-wagon-ftp
    - maven-wagon-http-lightweight
    - maven-wagon-javadoc
    - maven-wagon-providers
    - plexus-cipher-javadoc
    - plexus-classworlds-javadoc
    - plexus-containers
    - plexus-containers-component-javadoc
    - plexus-containers-component-metadata
    - plexus-containers-container-default
    - plexus-containers-javadoc
    - plexus-interpolation-javadoc
    - plexus-sec-dispatcher-javadoc
    - plexus-utils-javadoc
    - sisu-javadoc
    - slf4j-ext
    - slf4j-javadoc
    - slf4j-jcl
    - slf4j-jdk14
    - slf4j-log4j12
    - slf4j-manual
    - slf4j-sources
  artifacts:
    rpms:
    - slf4j-0:1.7.25-4.module+el8+2452+b359bfcd.noarch
    - slf4j-javadoc-0:1.7.25-4.module+el8+2452+b359bfcd.noarch
    - slf4j-manual-0:1.7.25-4.module+el8+2452+b359bfcd.noarch
    - slf4j-jdk14-0:1.7.25-4.module+el8+2452+b359bfcd.noarch
    - slf4j-log4j12-0:1.7.25-4.module+el8+2452+b359bfcd.noarch
    - slf4j-jcl-0:1.7.25-4.module+el8+2452+b359bfcd.noarch
    - slf4j-ext-0:1.7.25-4.module+el8+2452+b359bfcd.noarch
    - jcl-over-slf4j-0:1.7.25-4.module+el8+2452+b359bfcd.noarch
    - log4j-over-slf4j-0:1.7.25-4.module+el8+2452+b359bfcd.noarch
    - jul-to-slf4j-0:1.7.25-4.module+el8+2452+b359bfcd.noarch
    - slf4j-sources-0:1.7.25-4.module+el8+2452+b359bfcd.noarch
    - plexus-utils-0:3.1.0-3.module+el8+2452+b359bfcd.noarch
    - plexus-utils-javadoc-0:3.1.0-3.module+el8+2452+b359bfcd.noarch
    - plexus-interpolation-0:1.22-9.module+el8+2452+b359bfcd.noarch
    - plexus-interpolation-javadoc-0:1.22-9.module+el8+2452+b359bfcd.noarch
    - plexus-containers-0:1.7.1-8.module+el8+2452+b359bfcd.noarch
    - plexus-containers-component-metadata-0:1.7.1-8.module+el8+2452+b359bfcd.noarch
    - plexus-containers-component-javadoc-0:1.7.1-8.module+el8+2452+b359bfcd.noarch
    - plexus-containers-component-annotations-0:1.7.1-8.module+el8+2452+b359bfcd.noarch
    - plexus-containers-container-default-0:1.7.1-8.module+el8+2452+b359bfcd.noarch
    - plexus-containers-javadoc-0:1.7.1-8.module+el8+2452+b359bfcd.noarch
    - plexus-classworlds-0:2.5.2-9.module+el8+2452+b359bfcd.noarch
    - plexus-classworlds-javadoc-0:2.5.2-9.module+el8+2452+b359bfcd.noarch
    - plexus-cipher-0:1.7-14.module+el8+2452+b359bfcd.noarch
    - plexus-cipher-javadoc-0:1.7-14.module+el8+2452+b359bfcd.noarch
    - jsoup-0:1.11.3-3.module+el8+2452+b359bfcd.noarch
    - jsoup-javadoc-0:1.11.3-3.module+el8+2452+b359bfcd.noarch
    - jboss-interceptors-1.2-api-0:1.0.0-8.module+el8+2452+b359bfcd.noarch
    - jboss-interceptors-1.2-api-javadoc-0:1.0.0-8.module+el8+2452+b359bfcd.noarch
    - httpcomponents-core-0:4.4.10-3.module+el8+2452+b359bfcd.noarch
    - httpcomponents-core-javadoc-0:4.4.10-3.module+el8+2452+b359bfcd.noarch
    - hawtjni-0:1.16-2.module+el8+2452+b359bfcd.noarch
    - hawtjni-javadoc-0:1.16-2.module+el8+2452+b359bfcd.noarch
    - hawtjni-runtime-0:1.16-2.module+el8+2452+b359bfcd.noarch
    - maven-hawtjni-plugin-0:1.16-2.module+el8+2452+b359bfcd.noarch
    - guava20-0:20.0-8.module+el8+2452+b359bfcd.noarch
    - guava20-javadoc-0:20.0-8.module+el8+2452+b359bfcd.noarch
    - guava20-testlib-0:20.0-8.module+el8+2452+b359bfcd.noarch
    - glassfish-el-0:3.0.1-0.7.b08.module+el8+2452+b359bfcd.noarch
    - glassfish-el-api-0:3.0.1-0.7.b08.module+el8+2452+b359bfcd.noarch
    - glassfish-el-javadoc-0:3.0.1-0.7.b08.module+el8+2452+b359bfcd.noarch
    - geronimo-annotation-0:1.0-23.module+el8+2452+b359bfcd.noarch
    - geronimo-annotation-javadoc-0:1.0-23.module+el8+2452+b359bfcd.noarch
    - atinject-0:1-28.20100611svn86.module+el8+2452+b359bfcd.noarch
    - atinject-tck-0:1-28.20100611svn86.module+el8+2452+b359bfcd.noarch
    - atinject-javadoc-0:1-28.20100611svn86.module+el8+2452+b359bfcd.noarch
    - apache-commons-logging-0:1.2-13.module+el8+2452+b359bfcd.noarch
    - apache-commons-logging-javadoc-0:1.2-13.module+el8+2452+b359bfcd.noarch
    - apache-commons-lang3-0:3.7-3.module+el8+2452+b359bfcd.noarch
    - apache-commons-lang3-javadoc-0:3.7-3.module+el8+2452+b359bfcd.noarch
    - apache-commons-io-1:2.6-3.module+el8+2452+b359bfcd.noarch
    - apache-commons-io-javadoc-1:2.6-3.module+el8+2452+b359bfcd.noarch
    - apache-commons-codec-0:1.11-3.module+el8+2452+b359bfcd.noarch
    - apache-commons-codec-javadoc-0:1.11-3.module+el8+2452+b359bfcd.noarch
    - apache-commons-cli-0:1.4-4.module+el8+2452+b359bfcd.noarch
    - apache-commons-cli-javadoc-0:1.4-4.module+el8+2452+b359bfcd.noarch
    - aopalliance-0:1.0-17.module+el8+2452+b359bfcd.noarch
    - aopalliance-javadoc-0:1.0-17.module+el8+2452+b359bfcd.noarch
    - plexus-sec-dispatcher-0:1.4-26.module+el8+2452+b359bfcd.noarch
    - plexus-sec-dispatcher-javadoc-0:1.4-26.module+el8+2452+b359bfcd.noarch
    - maven-shared-utils-0:3.2.1-0.1.module+el8+2452+b359bfcd.noarch
    - maven-shared-utils-javadoc-0:3.2.1-0.1.module+el8+2452+b359bfcd.noarch
    - jansi-native-0:1.7-7.module+el8+2452+b359bfcd.x86_64
    - jansi-native-javadoc-0:1.7-7.module+el8+2452+b359bfcd.noarch
    - httpcomponents-client-0:4.5.5-4.module+el8+2452+b359bfcd.noarch
    - httpcomponents-client-cache-0:4.5.5-4.module+el8+2452+b359bfcd.noarch
    - httpcomponents-client-javadoc-0:4.5.5-4.module+el8+2452+b359bfcd.noarch
    - google-guice-0:4.1-11.module+el8+2452+b359bfcd.noarch
    - guice-parent-0:4.1-11.module+el8+2452+b359bfcd.noarch
    - guice-assistedinject-0:4.1-11.module+el8+2452+b359bfcd.noarch
    - guice-extensions-0:4.1-11.module+el8+2452+b359bfcd.noarch
    - guice-grapher-0:4.1-11.module+el8+2452+b359bfcd.noarch
    - guice-jmx-0:4.1-11.module+el8+2452+b359bfcd.noarch
    - guice-jndi-0:4.1-11.module+el8+2452+b359bfcd.noarch
    - guice-servlet-0:4.1-11.module+el8+2452+b359bfcd.noarch
    - guice-multibindings-0:4.1-11.module+el8+2452+b359bfcd.noarch
    - guice-testlib-0:4.1-11.module+el8+2452+b359bfcd.noarch
    - guice-bom-0:4.1-11.module+el8+2452+b359bfcd.noarch
    - guice-throwingproviders-0:4.1-11.module+el8+2452+b359bfcd.noarch
    - google-guice-javadoc-0:4.1-11.module+el8+2452+b359bfcd.noarch
    - cdi-api-0:1.2-8.module+el8+2452+b359bfcd.noarch
    - cdi-api-javadoc-0:1.2-8.module+el8+2452+b359bfcd.noarch
    - sisu-inject-1:0.3.3-6.module+el8+2452+b359bfcd.noarch
    - sisu-plexus-1:0.3.3-6.module+el8+2452+b359bfcd.noarch
    - sisu-javadoc-1:0.3.3-6.module+el8+2452+b359bfcd.noarch
    - maven-wagon-0:3.1.0-1.module+el8+2452+b359bfcd.noarch
    - maven-wagon-provider-api-0:3.1.0-1.module+el8+2452+b359bfcd.noarch
    - maven-wagon-providers-0:3.1.0-1.module+el8+2452+b359bfcd.noarch
    - maven-wagon-file-0:3.1.0-1.module+el8+2452+b359bfcd.noarch
    - maven-wagon-ftp-0:3.1.0-1.module+el8+2452+b359bfcd.noarch
    - maven-wagon-http-0:3.1.0-1.module+el8+2452+b359bfcd.noarch
    - maven-wagon-http-shared-0:3.1.0-1.module+el8+2452+b359bfcd.noarch
    - maven-wagon-http-lightweight-0:3.1.0-1.module+el8+2452+b359bfcd.noarch
    - maven-wagon-javadoc-0:3.1.0-1.module+el8+2452+b359bfcd.noarch
    - jansi-0:1.17.1-1.module+el8+2452+b359bfcd.noarch
    - jansi-javadoc-0:1.17.1-1.module+el8+2452+b359bfcd.noarch
    - maven-resolver-1:1.1.1-2.module+el8+2452+b359bfcd.noarch
    - maven-resolver-api-1:1.1.1-2.module+el8+2452+b359bfcd.noarch
    - maven-resolver-spi-1:1.1.1-2.module+el8+2452+b359bfcd.noarch
    - maven-resolver-util-1:1.1.1-2.module+el8+2452+b359bfcd.noarch
    - maven-resolver-impl-1:1.1.1-2.module+el8+2452+b359bfcd.noarch
    - maven-resolver-test-util-1:1.1.1-2.module+el8+2452+b359bfcd.noarch
    - maven-resolver-connector-basic-1:1.1.1-2.module+el8+2452+b359bfcd.noarch
    - maven-resolver-transport-classpath-1:1.1.1-2.module+el8+2452+b359bfcd.noarch
    - maven-resolver-transport-file-1:1.1.1-2.module+el8+2452+b359bfcd.noarch
    - maven-resolver-transport-http-1:1.1.1-2.module+el8+2452+b359bfcd.noarch
    - maven-resolver-transport-wagon-1:1.1.1-2.module+el8+2452+b359bfcd.noarch
    - maven-resolver-javadoc-1:1.1.1-2.module+el8+2452+b359bfcd.noarch
    - maven-1:3.5.4-5.module+el8+2452+b359bfcd.noarch
    - maven-lib-1:3.5.4-5.module+el8+2452+b359bfcd.noarch
...
---
document: modulemd
version: 2
data:
  name: mariadb
  stream: '10.3'
  version: '820190314153642'
  context: 9edba152
  arch: x86_64
  license:
    content:
    - GPLv2
    - GPLv2 with exceptions and LGPLv2 and BSD.
    - LGPLv2+
    module:
    - MIT
  summary: MariaDB Module
  description: MariaDB is a community developed branch of MySQL. MariaDB is a multi-user,
    multi-threaded SQL database server. It is a client/server implementation consisting
    of a server daemon (mysqld) and many different client programs and libraries.
    The base package contains the standard MariaDB/MySQL client programs and generic
    MySQL files.
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  api:
    rpms:
    - mariadb
    - mariadb-server
  components:
    rpms:
      Judy:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 4
        rationale: MariaDB dependency for OQgraph computation engine
        ref: stream-mariadb-10.3-rhel-8.0.0
      asio:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 12
        rationale: Galera dependency for asynchronous I/O operation
        ref: stream-mariadb-10.3-rhel-8.0.0
      galera:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 16
        rationale: Galera package for MariaDB server replication
        ref: stream-10.3-rhel-8.0.0
      mariadb:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 8
        rationale: MariaDB package
        ref: stream-10.3-rhel-8.0.0
  buildopts:
    rpms:
      macros: '%runselftest 1

        %ignore_testsuite_result 0

        '
  references:
    community: http://mariadb.org
    documentation: https://mariadb.com/kb/en/library/documentation/
    tracker: http://bugzilla.redhat.com
  profiles:
    client:
      rpms:
      - mariadb
    galera:
      rpms:
      - mariadb-server
      - mariadb-server-galera
    server:
      rpms:
      - mariadb-server
  filter:
    rpms:
    - Judy-devel
    - asio-devel
  artifacts:
    rpms:
    - Judy-0:1.0.5-18.module+el8+2885+7b8bb354.x86_64
    - Judy-devel-0:1.0.5-18.module+el8+2885+7b8bb354.x86_64
    - Judy-debugsource-0:1.0.5-18.module+el8+2885+7b8bb354.x86_64
    - Judy-debuginfo-0:1.0.5-18.module+el8+2885+7b8bb354.x86_64
    - mariadb-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-common-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-errmsg-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-server-galera-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-server-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-oqgraph-engine-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-backup-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-gssapi-server-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-server-utils-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-devel-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-embedded-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-embedded-devel-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-test-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-debugsource-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-debuginfo-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-server-debuginfo-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-oqgraph-engine-debuginfo-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-backup-debuginfo-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-gssapi-server-debuginfo-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-server-utils-debuginfo-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-embedded-debuginfo-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - mariadb-test-debuginfo-3:10.3.27-3.module+el8+2885+7b8bb354.x86_64
    - asio-devel-0:1.10.8-7.module+el8+2885+7b8bb354.x86_64
    - galera-0:25.3.31-1.module+el8+2885+7b8bb354.x86_64
    - galera-debugsource-0:25.3.31-1.module+el8+2885+7b8bb354.x86_64
    - galera-debuginfo-0:25.3.31-1.module+el8+2885+7b8bb354.x86_64
...
---
document: modulemd
version: 2
data:
  name: mailman
  stream: '2.1'
  version: '8030020200601095048'
  context: c307c522
  arch: x86_64
  license:
    content:
    - GPLv2+
    module:
    - MIT
  summary: Electronic mail discussion and e-newsletter lists managing software
  description: An initial version of the mailman mailing list management software
  dependencies:
  - buildrequires:
      platform:
      - el8
      python27:
      - 2.7
    requires:
      platform:
      - el8
      python27:
      - 2.7
  api:
    rpms:
    - mailman
  components:
    rpms:
      mailman:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        rationale: Module API.
        ref: stream-2.1-rhel-8.3.0
  references:
    documentation: https://launchpad.net/mailman
    tracker: https://bugs.launchpad.net/mailman
  profiles:
    common:
      rpms:
      - mailman
  filter:
    rpms:
    - python3-dns
  artifacts:
    rpms:
    - mailman-3:2.1.29-10.module+el8.3.0+6860+8e47d84b.x86_64
    - mailman-debugsource-3:2.1.29-10.module+el8.3.0+6860+8e47d84b.x86_64
    - mailman-debuginfo-3:2.1.29-10.module+el8.3.0+6860+8e47d84b.x86_64
...
---
document: modulemd
version: 2
data:
  name: libselinux-python
  stream: '2.8'
  version: '8020020190916085518'
  context: b0d89eb3
  arch: x86_64
  license:
    content:
    - Public Domain
    module:
    - MIT
  summary: Python 2 bindings for libselinux
  description: The libselinux-python package contains the python bindings for developing
    SELinux applications.
  dependencies:
  - buildrequires:
      platform:
      - el8
      python27:
      - 2.7
    requires:
      platform:
      - el8
      python27:
      - 2.7
  api:
    rpms:
    - libselinux-python
  components:
    rpms:
      libselinux:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Provides libselinux python bindings
        ref: rhel-8.1.0
  buildopts:
    rpms:
      macros: '%with_python2 1

        '
  profiles:
    common:
      rpms:
      - libselinux-python
  filter:
    rpms:
    - libselinux
    - libselinux-debugsource
    - libselinux-devel
    - libselinux-ruby
    - libselinux-ruby-debuginfo
    - libselinux-static
    - libselinux-utils
    - libselinux-utils-debuginfo
    - python3-libselinux
    - python3-libselinux-debuginfo
  artifacts:
    rpms:
    - libselinux-static-0:2.9-2.1.module+el8.1.0+3972+45ab4324.x86_64
    - python3-libselinux-0:2.9-2.1.module+el8.1.0+3972+45ab4324.x86_64
    - libselinux-debuginfo-0:2.9-2.1.module+el8.1.0+3972+45ab4324.x86_64
    - python3-libselinux-debuginfo-0:2.9-2.1.module+el8.1.0+3972+45ab4324.x86_64
    - libselinux-utils-0:2.9-2.1.module+el8.1.0+3972+45ab4324.x86_64
    - libselinux-python-0:2.9-2.1.module+el8.1.0+3972+45ab4324.x86_64
    - libselinux-utils-debuginfo-0:2.9-2.1.module+el8.1.0+3972+45ab4324.x86_64
    - libselinux-ruby-debuginfo-0:2.9-2.1.module+el8.1.0+3972+45ab4324.x86_64
    - libselinux-python-debuginfo-0:2.9-2.1.module+el8.1.0+3972+45ab4324.x86_64
    - libselinux-ruby-0:2.9-2.1.module+el8.1.0+3972+45ab4324.x86_64
    - libselinux-0:2.9-2.1.module+el8.1.0+3972+45ab4324.x86_64
    - libselinux-debugsource-0:2.9-2.1.module+el8.1.0+3972+45ab4324.x86_64
    - libselinux-devel-0:2.9-2.1.module+el8.1.0+3972+45ab4324.x86_64
...
---
document: modulemd
version: 2
data:
  name: ant
  stream: '1.10'
  version: '820181213135032'
  context: 5ea3b708
  arch: x86_64
  license:
    content:
    - ASL 2.0
    module:
    - MIT
  summary: Java build tool
  description: Apache Ant is a Java library and command-line tool whose mission is
    to drive processes described in build files as targets and extension points dependent
    upon each other. The main known usage of Ant is the build of Java applications.
    Ant supplies a number of built-in tasks allowing to compile, assemble, test and
    run Java applications. Ant can also be used effectively to build non Java applications,
    for instance C or C++ applications. More generally, Ant can be used to pilot any
    type of process which can be described in terms of targets and tasks.
  dependencies:
  - buildrequires:
      javapackages-tools:
      - 201801
      platform:
      - el8
    requires:
      platform: []
  api:
    rpms:
    - ant
  components:
    rpms:
      ant:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/ant
        rationale: 'Module API.

          '
        ref: stream-ant-1.10
        repository: git://pkgs.devel.redhat.com/rpms/ant
  buildopts:
    rpms:
      macros: '%_with_xmvn_javadoc 1

        %_without_asciidoc 1

        %_without_avalon 1

        %_without_bouncycastle 1

        %_without_cython 1

        %_without_dafsa 1

        %_without_desktop 1

        %_without_doxygen 1

        %_without_dtd 1

        %_without_eclipse 1

        %_without_ehcache 1

        %_without_emacs 1

        %_without_equinox 1

        %_without_fop 1

        %_without_ftp 1

        %_without_gradle 1

        %_without_groovy 1

        %_without_hadoop 1

        %_without_hsqldb 1

        %_without_itext 1

        %_without_jackson 1

        %_without_jmh 1

        %_without_jna 1

        %_without_jpa 1

        %_without_junit5 1

        %_without_logback 1

        %_without_markdown 1

        %_without_memcached 1

        %_without_memoryfilesystem 1

        %_without_obr 1

        %_without_python 1

        %_without_reporting 1

        %_without_scm 1

        %_without_snappy 1

        %_without_spring 1

        %_without_ssh 1

        %_without_testlib 1

        '
  references:
    community: https://ant.apache.org/
  profiles:
    common:
      rpms:
      - ant
  filter:
    rpms:
    - ant-antlr
    - ant-apache-bcel
    - ant-apache-bsf
    - ant-apache-log4j
    - ant-apache-oro
    - ant-apache-regexp
    - ant-apache-resolver
    - ant-apache-xalan2
    - ant-commons-logging
    - ant-commons-net
    - ant-javadoc
    - ant-javamail
    - ant-jdepend
    - ant-jmf
    - ant-jsch
    - ant-junit
    - ant-manual
    - ant-swing
    - ant-testutil
    - ant-xz
  artifacts:
    rpms:
    - ant-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-lib-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-jmf-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-swing-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-antlr-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-apache-bsf-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-apache-resolver-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-commons-logging-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-commons-net-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-apache-bcel-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-apache-log4j-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-apache-oro-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-apache-regexp-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-apache-xalan2-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-javamail-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-jdepend-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-jsch-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-junit-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-testutil-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-xz-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-manual-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-javadoc-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
...
---
document: modulemd
version: 2
data:
  name: freeradius
  stream: '3.0'
  version: '8030020200806223029'
  context: 1e4bbb35
  arch: x86_64
  license:
    content:
    - GPLv2+ and LGPLv2+
    module:
    - GPL
  summary: High-performance and highly configurable free RADIUS server
  description: 'The FreeRADIUS Server Project is a high performance and highly configurable
    GPL''d free RADIUS server. The server is similar in some respects to Livingston''s
    2.0 server.  While FreeRADIUS started as a variant of the Cistron RADIUS server,
    they don''t share a lot in common any more. It now has many more features than
    Cistron or Livingston, and is much more configurable.

    FreeRADIUS is an Internet authentication daemon, which implements the RADIUS protocol,
    as defined in RFC 2865 (and others). It allows Network Access Servers (NAS boxes)
    to perform authentication for dial-up users. There are also RADIUS clients available
    for Web servers, firewalls, Unix logins, and more.  Using RADIUS allows authentication
    and authorization for a network to be centralized, and minimizes the amount of
    re-configuration which has to be done when adding or deleting new users.'
  dependencies:
  - buildrequires:
      perl:
      - 5.26
      platform:
      - el8
    requires:
      perl:
      - 5.26
      platform:
      - el8
  api:
    rpms:
    - freeradius
    - freeradius-devel
    - freeradius-doc
    - freeradius-krb5
    - freeradius-ldap
    - freeradius-mysql
    - freeradius-perl
    - freeradius-postgresql
    - freeradius-rest
    - freeradius-sqlite
    - freeradius-unixODBC
    - freeradius-utils
  components:
    rpms:
      freeradius:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        rationale: Provides the FreeRADIUS server
        ref: stream-3.0-rhel-8.3.0
  profiles:
    server:
      description: The FreeRADIUS Server
      rpms:
      - freeradius
  artifacts:
    rpms:
    - freeradius-postgresql-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-postgresql-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-perl-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-ldap-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-unixODBC-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-utils-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-rest-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - python3-freeradius-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-krb5-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-utils-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-perl-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-sqlite-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-devel-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-debugsource-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-doc-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-rest-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-unixODBC-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - python3-freeradius-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-sqlite-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-mysql-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-ldap-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-krb5-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-mysql-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
...
---
document: modulemd
version: 2
data:
  name: gimp
  stream: '2.8'
  version: '820181213135540'
  context: 77fc8825
  arch: x86_64
  license:
    content:
    - GPLv3+ and GPLv3
    - LGPLv2+
    - LGPLv2+, MIT
    - LGPLv3+
    - MPLv1.1 or LGPLv2
    module:
    - MIT
  summary: gimp module
  description: 'GIMP (GNU Image Manipulation Program) is a powerful image composition
    and

    editing program, which can be extremely useful for creating logos and other

    graphics for webpages. '
  dependencies:
  - buildrequires:
      platform:
      - el8
      python27:
      - 2.7
    requires:
      platform:
      - el8
      python27:
      - 2.7
  api:
    rpms:
    - gimp
    - gimp-devel
    - gimp-devel-tools
    - gimp-libs
  components:
    rpms:
      gimp:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        cache: http://pkgs.devel.redhat.com/repo/pkgs/gimp
        rationale: GIMP Module.
        ref: stream-2.8
        repository: git://pkgs.devel.redhat.com/rpms/gimp
      pygobject2:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 1
        cache: http://pkgs.devel.redhat.com/repo/pkgs/pygobject2
        rationale: GIMP Module dependency
        ref: stream-2.28.7
        repository: git://pkgs.devel.redhat.com/rpms/pygobject2
      pygtk2:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 5
        cache: http://pkgs.devel.redhat.com/repo/pkgs/pygtk2
        rationale: GIMP Module dependency
        ref: stream-2.24
        repository: git://pkgs.devel.redhat.com/rpms/pygtk2
      python2-pycairo:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 3
        cache: http://pkgs.devel.redhat.com/repo/pkgs/python2-pycairo
        rationale: Python2 binding required by pygtk2
        ref: stream-python2
        repository: git://pkgs.devel.redhat.com/rpms/python2-pycairo
  references:
    community: https://www.gimp.org/develop/
    documentation: https://www.gimp.org/docs/
    tracker: https://www.gimp.org/bugs/
  profiles:
    common:
      rpms:
      - gimp
    devel:
      rpms:
      - gimp-devel
      - gimp-devel-tools
  artifacts:
    rpms:
    - ant-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-lib-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-jmf-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-swing-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-antlr-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-apache-bsf-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-apache-resolver-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-commons-logging-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-commons-net-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-apache-bcel-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-apache-log4j-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-apache-oro-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-apache-regexp-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-apache-xalan2-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-javamail-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-jdepend-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-jsch-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-junit-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-testutil-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-xz-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-manual-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - ant-javadoc-0:1.10.5-1.module+el8+2438+c99a8a1.noarch
    - pygobject2-0:2.28.7-4.module+el8+2760+3d7d61b2.x86_64
    - pygobject2-codegen-0:2.28.7-4.module+el8+2760+3d7d61b2.x86_64
    - pygobject2-devel-0:2.28.7-4.module+el8+2760+3d7d61b2.x86_64
    - pygobject2-doc-0:2.28.7-4.module+el8+2760+3d7d61b2.x86_64
    - pygobject2-debugsource-0:2.28.7-4.module+el8+2760+3d7d61b2.x86_64
    - pygobject2-debuginfo-0:2.28.7-4.module+el8+2760+3d7d61b2.x86_64
    - python2-cairo-0:1.16.3-6.module+el8+2760+3d7d61b2.x86_64
    - python2-cairo-devel-0:1.16.3-6.module+el8+2760+3d7d61b2.x86_64
    - python2-pycairo-debugsource-0:1.16.3-6.module+el8+2760+3d7d61b2.x86_64
    - python2-cairo-debuginfo-0:1.16.3-6.module+el8+2760+3d7d61b2.x86_64
    - pygtk2-0:2.24.0-24.module+el8+2760+3d7d61b2.x86_64
    - pygtk2-codegen-0:2.24.0-24.module+el8+2760+3d7d61b2.x86_64
    - pygtk2-devel-0:2.24.0-24.module+el8+2760+3d7d61b2.x86_64
    - pygtk2-doc-0:2.24.0-24.module+el8+2760+3d7d61b2.noarch
    - pygtk2-debugsource-0:2.24.0-24.module+el8+2760+3d7d61b2.x86_64
    - pygtk2-debuginfo-0:2.24.0-24.module+el8+2760+3d7d61b2.x86_64
    - gimp-2:2.8.22-15.module+el8+2760+3d7d61b2.x86_64
    - gimp-libs-2:2.8.22-15.module+el8+2760+3d7d61b2.x86_64
    - gimp-devel-2:2.8.22-15.module+el8+2760+3d7d61b2.x86_64
    - gimp-devel-tools-2:2.8.22-15.module+el8+2760+3d7d61b2.x86_64
    - gimp-debugsource-2:2.8.22-15.module+el8+2760+3d7d61b2.x86_64
    - gimp-debuginfo-2:2.8.22-15.module+el8+2760+3d7d61b2.x86_64
    - gimp-libs-debuginfo-2:2.8.22-15.module+el8+2760+3d7d61b2.x86_64
    - gimp-devel-tools-debuginfo-2:2.8.22-15.module+el8+2760+3d7d61b2.x86_64
...
---
document: modulemd
version: 2
data:
  name: httpd
  stream: '2.4'
  version: '8030020200818000036'
  context: 30b713e6
  arch: x86_64
  license:
    content:
    - ASL 2.0
    module:
    - MIT
  summary: Apache HTTP Server
  description: Apache httpd is a powerful, efficient, and extensible HTTP server.
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform:
      - el8
  api:
    rpms:
    - httpd
    - httpd-devel
    - httpd-filesystem
    - mod_ssl
  components:
    rpms:
      httpd:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 10
        rationale: Apache httpd
        ref: stream-2.4-rhel-8.3.0
      mod_http2:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 20
        rationale: HTTP/2 support for Apache httpd
        ref: stream-2.4-rhel-8.3.0
      mod_md:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        buildorder: 20
        rationale: Certificate provisioning using ACME for Apache httpd
        ref: stream-2.4-rhel-8.3.0
  references:
    documentation: https://httpd.apache.org/docs/2.4/
    tracker: https://bz.apache.org/bugzilla/
  profiles:
    common:
      rpms:
      - httpd
      - httpd-filesystem
      - httpd-tools
      - mod_http2
      - mod_ssl
    devel:
      rpms:
      - httpd
      - httpd-devel
      - httpd-filesystem
      - httpd-tools
    minimal:
      rpms:
      - httpd
  artifacts:
    rpms:
    - httpd-tools-debuginfo-0:2.4.37-30.module+el8.3.0+7001+0766b9e7.x86_64
    - httpd-filesystem-0:2.4.37-30.module+el8.3.0+7001+0766b9e7.noarch
    - httpd-debugsource-0:2.4.37-30.module+el8.3.0+7001+0766b9e7.x86_64
    - httpd-0:2.4.37-30.module+el8.3.0+7001+0766b9e7.x86_64
    - mod_session-0:2.4.37-30.module+el8.3.0+7001+0766b9e7.x86_64
    - mod_proxy_html-debuginfo-1:2.4.37-30.module+el8.3.0+7001+0766b9e7.x86_64
    - httpd-tools-0:2.4.37-30.module+el8.3.0+7001+0766b9e7.x86_64
    - mod_ldap-debuginfo-0:2.4.37-30.module+el8.3.0+7001+0766b9e7.x86_64
    - httpd-devel-0:2.4.37-30.module+el8.3.0+7001+0766b9e7.x86_64
    - httpd-manual-0:2.4.37-30.module+el8.3.0+7001+0766b9e7.noarch
    - mod_ssl-1:2.4.37-30.module+el8.3.0+7001+0766b9e7.x86_64
    - mod_session-debuginfo-0:2.4.37-30.module+el8.3.0+7001+0766b9e7.x86_64
    - mod_ldap-0:2.4.37-30.module+el8.3.0+7001+0766b9e7.x86_64
    - mod_ssl-debuginfo-1:2.4.37-30.module+el8.3.0+7001+0766b9e7.x86_64
    - httpd-debuginfo-0:2.4.37-30.module+el8.3.0+7001+0766b9e7.x86_64
    - mod_proxy_html-1:2.4.37-30.module+el8.3.0+7001+0766b9e7.x86_64
    - freeradius-postgresql-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-postgresql-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-perl-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-ldap-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-unixODBC-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-utils-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-rest-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - python3-freeradius-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-krb5-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-utils-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-perl-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-sqlite-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-devel-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-debugsource-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-doc-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-rest-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-unixODBC-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - python3-freeradius-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-sqlite-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-mysql-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-ldap-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-krb5-debuginfo-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - freeradius-mysql-0:3.0.20-3.module+el8.3.0+7597+67902674.x86_64
    - mod_md-debugsource-1:2.0.8-8.module+el8.3.0+7001+0766b9e7.x86_64
    - mod_md-1:2.0.8-8.module+el8.3.0+7001+0766b9e7.x86_64
    - mod_md-debuginfo-1:2.0.8-8.module+el8.3.0+7001+0766b9e7.x86_64
    - mod_http2-debuginfo-0:1.15.7-2.module+el8.3.0+7001+0766b9e7.x86_64
    - mod_http2-debugsource-0:1.15.7-2.module+el8.3.0+7001+0766b9e7.x86_64
    - mod_http2-0:1.15.7-2.module+el8.3.0+7001+0766b9e7.x86_64
...
---
document: modulemd
version: 2
data:
  name: javapackages-runtime
  stream: '201801'
  version: '820181213140046'
  context: 302ab70f
  arch: x86_64
  license:
    content:
    - BSD
    module:
    - MIT
  summary: Basic runtime utilities to support Java applications
  description: This module contains basic filesystem layout and runtime utilities
    used to support system applications written in JVM languages.
  dependencies:
  - buildrequires:
      platform:
      - el8
    requires:
      platform: []
  api:
    rpms:
    - javapackages-filesystem
    - javapackages-tools
  components:
    rpms:
      javapackages-tools:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        cache: http://pkgs.devel.redhat.com/repo/pkgs/javapackages-tools
        rationale: 'Module API.

          '
        ref: stream-javapackages-runtime-201801
        repository: git://pkgs.devel.redhat.com/rpms/javapackages-tools
  buildopts:
    rpms:
      macros: '%_without_asciidoc 1

        %_without_gradle 1

        '
  profiles:
    common:
      rpms:
      - javapackages-filesystem
      - javapackages-tools
  filter:
    rpms:
    - ivy-local
    - javapackages-local
    - maven-local
    - python3-javapackages
  artifacts:
    rpms:
    - javapackages-tools-0:5.3.0-1.module+el8+2447+6f56d9a6.noarch
    - javapackages-filesystem-0:5.3.0-1.module+el8+2447+6f56d9a6.noarch
    - ivy-local-0:5.3.0-1.module+el8+2447+6f56d9a6.noarch
    - javapackages-local-0:5.3.0-1.module+el8+2447+6f56d9a6.noarch
    - maven-local-0:5.3.0-1.module+el8+2447+6f56d9a6.noarch
    - python3-javapackages-0:5.3.0-1.module+el8+2447+6f56d9a6.noarch
...
---
document: modulemd
version: 2
data:
  name: inkscape
  stream: 0.92.3
  version: '8010020191118144808'
  context: 656b880e
  arch: x86_64
  license:
    content:
    - ASL 2.0
    - GPLv2+ and CC-BY
    module:
    - GPL-2.0
  summary: Vector-based drawing program using SVG
  description: 'Inkscape is a vector graphics editor, with capabilities similar to

    Illustrator, CorelDraw, or Xara X, using the W3C standard Scalable Vector

    Graphics (SVG) file format.  It is therefore a very useful tool for web

    designers and as an interchange format for desktop publishing.


    Inkscape supports many advanced SVG features (markers, clones, alpha

    blending, etc.) and great care is taken in designing a streamlined

    interface. It is very easy to edit nodes, perform complex path operations,

    trace bitmaps and much more.'
  dependencies:
  - buildrequires:
      platform:
      - el8
      python27:
      - 2.7
    requires:
      platform:
      - el8
      python27:
      - 2.7
  api:
    rpms:
    - inkscape
  components:
    rpms:
      inkscape:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Module API.
        ref: stream-0.92.3-rhel-8.1.0
      python-scour:
        arches:
        - aarch64
        - i686
        - ppc64le
        - s390x
        - x86_64
        rationale: Runtime requirement of inkscape, should not be in API.
        ref: stream-0.35
  buildopts:
    rpms:
      macros: '%_with_python2 1

        '
  references:
    documentation: https://inkscape.org/en/learn/
    tracker: https://bugs.launchpad.net/inkscape
  profiles:
    common:
      rpms:
      - inkscape
  filter:
    rpms:
    - python3-*
    - python3-dns
    - python3-scour
  artifacts:
    rpms:
    - python2-scour-0:0.35-9.module+el8.1.0+4737+97b227b1.noarch
    - python3-scour-0:0.35-9.module+el8.1.0+4737+97b227b1.noarch
    - inkscape-0:0.92.3-12.module+el8.1.0+4737+97b227b1.x86_64
    - inkscape-view-0:0.92.3-12.module+el8.1.0+4737+97b227b1.x86_64
    - inkscape-docs-0:0.92.3-12.module+el8.1.0+4737+97b227b1.x86_64
    - inkscape-debugsource-0:0.92.3-12.module+el8.1.0+4737+97b227b1.x86_64
    - inkscape-debuginfo-0:0.92.3-12.module+el8.1.0+4737+97b227b1.x86_64
    - inkscape-view-debuginfo-0:0.92.3-12.module+el8.1.0+4737+97b227b1.x86_64
...
