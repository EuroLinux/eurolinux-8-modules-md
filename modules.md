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
---
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
