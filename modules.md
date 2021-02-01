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
