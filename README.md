## sqldeveloper-package for Debian and derivatives

**`sqldeveloper-package`** is a small script that will build a [_Debian_](http://www.debian.org) [_package_](http://www.wikipedia.org/wiki/Deb_%28file_format%29) from [_Oracle_](http://www.oracle.com)_'s_ [_SQL Developer_](http://www.oracle.com/technetwork/developer-tools/sql-developer/).

This utility makes it possible to build a _Debian_ package of _Oracle SQL Developer_. The _Oracle SQL Developer_ program is governed by the copyright holder (_Oracle USA, Inc._), so you may be limited as to what you can do with the resulting package (i.e. no redistribution, etc). This utility will simply help you create the _Debian_ package, it is your responsibility to use the resulting package acordingly with the [_OTN license_](http://www.oracle.com/technetwork/licenses/sqldev-license-152021.html), a copy of which is included in the created package, that you must agree on when downloading the source.

This utility will require you to download the **architecture independent** archive from [_\<http://www.oracle.com/technetwork/developer-tools/sql-developer\>_](http://www.oracle.com/technetwork/developer-tools/sql-developer), identified as "**_Oracle SQL Developer for other platforms_**", "**_Oracle SQL Developer for Multiple Platforms_**" or "**_Oracle SQL Developer for Linux and Unix_**" (depending on which version you are building), to create the _Debian_ package from.

<hr width="40%">

<u>The <em>Debian Package</em> <strong><em>sqldeveloper-package</em></strong></u>

In order to run _Oracle SQL Developer_ you'll need a full working [_JDK_](http://www.wikipedia.org/wiki/JDK). The versions that are compatible with _SQL Developer_ are any [_JDK 1.5.0_](http://www.oracle.com/technetwork/java/javasebusiness/downloads/java-archive-downloads-javase5-419410.html)_\_06_ or above or [_JDK 1.6.0_](http://www.oracle.com/technetwork/java/javasebusiness/downloads/java-archive-downloads-javase6-419409.html)_\_03_ or above for _SQL Developer_ versions up to [_1.5.5_](http://www.oracle.com/technetwork/testcontent/index-archive155-099981.html). _SQL Developer_ versions from [_2.1_](http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/index-archive21-092243.html) to [_3.1_](http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/sqldev-31-download-1734499.html) are compatible with [_JDK 1.6.0_](http://www.oracle.com/technetwork/java/javasebusiness/downloads/java-archive-downloads-javase6-419409.html)_\_11_ or above and _SQL Developer_ version [_3.2_](http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/sqldev-downloads-v322-2080107.html) is compatible with [_JDK 1.6.0_](http://www.oracle.com/technetwork/java/javasebusiness/downloads/java-archive-downloads-javase6-419409.html)_\_04_ or above. _SQL Developer_ version [_4.0_](http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/sqldev-downloads-v4-2137727.html) is compatible with [_JDK 1.7.0_](http://www.oracle.com/technetwork/java/javase/downloads/java-archive-downloads-javase7-521261.html) series and _SQL Developer_ versions from [_4.1_](http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/sqldev-downloads-41-2592723.html) to [_17.3_](http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/index.html) are compatible with [_JDK 1.8.0_](http://www.oracle.com/technetwork/java/javase/downloads/java-archive-javase8-2177648.html) series.

<u><strong>Note</strong> that <em>Oracle SQL Developer</em> prior to version <a href="http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/sqldev-downloads-v4-2137727.html"><em>4.0</em></a> is <strong>not</strong> compatible with <a href="http://www.oracle.com/technetwork/java/javase/downloads/java-archive-downloads-javase7-521261.html"><em>JDK 1.7</em></a> (<em>JDK7.0</em>) or newer.


There are several ways to obtain a **compatible** _JDK_:
- install [_`default-jdk`_](http://packages.debian.org/search?searchon=names&exact=1&suite=all&section=all&keywords=default-jdk) (java), making sure it depends on the required _JDK_ version
- install one of the required [_`openjdk-6-jdk`_](http://packages.debian.org/search?searchon=names&exact=1&suite=all&section=all&keywords=openjdk-6-jdk), [_`openjdk-7-jdk`_](http://packages.debian.org/search?searchon=names&exact=1&suite=all&section=all&keywords=openjdk-7-jdk) or [_`openjdk-8-jdk`_](http://packages.debian.org/search?searchon=names&exact=1&suite=all&section=all&keywords=openjdk-8-jdk) (java)
- install the meta-package _`java-sdk`_, making sure that it installs the required _JDK_ version as dependency
- install one of the meta-packages _`java6-sdk`_, _`java7-sdk`_ or _`java8-sdk`_, making sure that it installs the required _JDK_ version as dependency
- download and run the installer for the version you wish to install from _Oracle_ [_&lt;http://www.oracle.com/technetwork/java/javase/downloads/&gt;_](http://www.oracle.com/technetwork/java/javase/downloads/)
- install [_`java-package`_](http://packages.debian.org/search?searchon=names&exact=1&suite=all&section=all&keywords=java-package) (contrib/misc) and generate a _Debian_ package from the above installer

After installing a **compatible** _JDK_ simply launch _SQL Developer_ through the [_graphical interface_](http://www.wikipedia.org/wiki/Desktop_Linux) or by invoking `/usr/bin/sqldeveloper` and supply the path where the _JDK_ was installed when prompted.

<hr width="40%">

### **Version History**

####### <u>Version <strong>0.2.3</strong></u>

