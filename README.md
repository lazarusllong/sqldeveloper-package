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

<a href="https://github.com/lazarusllong/sqldeveloper-package/releases/tag/0.3.0"><u>Version <strong>0.3.0</strong></u></a>
- **changelog:**
- **downloads:**

<a href="https://github.com/lazarusllong/sqldeveloper-package/releases/tag/0.2.4"><u>Version <strong>0.2.4</strong></u></a>
- **changelog:**
- **downloads:**

<a href="https://github.com/lazarusllong/sqldeveloper-package/releases/tag/0.2.3+nmu1"><u>Version <strong>0.2.3+nmu1</strong></u></a>
- **changelog:**
- **downloads:**

##### [Version 0.2.3](https://github.com/lazarusllong/sqldeveloper-package/releases/tag/0.2.3):
- **changelog:**
  - Fixed the command line options `-m`\|`--maintainer` option which was not getting the current login
- **downloads:**
  - [**`sqldeveloper-package\_0.2.3\_all.deb`**](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.2.3/sqldeveloper-package_0.2.3_all.deb) (_binary package_)
  - [`sqldeveloper-package\_0.2.3.dsc`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.2.3/sqldeveloper-package_0.2.3.dsc) (_source description file_)
  - [`sqldeveloper-package\_0.2.3.tar.gz`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.2.3/sqldeveloper-package_0.2.3.tar.gz) (_source code archive_)]

##### _Version 0.2.2_:
- **changelog:**
  - Modified `make-sqldeveloper-package` to not default to the author name and email for the _Maintainer:_ field of the _Debian_ package as follows: if command line options `-m`\|`--maintainer` and/or `-e`\|`--email` are set then use these, else if `DEBFULLNAME` and/or `DEBEMAIL` environment variables are set then use these, else default the _Maintainer_ name to an empty string and/or generate the _Maintainer_ email from the current login and hostname
- **downloads:**
  - _(unpublished)_

<u>Version <strong>0.2.1</strong></u>
- **changelog:**
  - Rearranged `make-sqldeveloper-package` help output to fit without wrapping in 80 columns
  - Rewrote the `sqldeveloper` wrapper script fixing all issues reported by `checkbashisms`
  - Modified the versioning of the resulting _Debian_ package to include the version of `make-sqldeveloper-package` used to build it
  - Changed the _Priority:_ from `optional` to `extra` for the resulting _Debian_ package
  - Modified the `make-sqldeveloper-package` to honor the `DEBFULLNAME` and `DEBEMAIL` environment variables for the _Maintainer:_ field of the _Debian_ package as follows: if command line options `-m`\|`--maintainer` and/or `-e`\|`--email` are set then use these, else if `DEBFULLNAME` and/or `DEBEMAIL` environment variables are set then use these, else default to the author name and email
  - Changed all negative exit and return values to positive integers
- **downloads:**
  - _(unpublished)_

<u>Version <strong>0.2.0</strong></u>
- **changelog:**
  - Rewrote the `make-sqldeveloper-package` fixing all issues reported by `checkbashisms` (thanks to [_Nelson A. de Oliveira_](mailto:naoliv@debian.org) who reported this)
  - Added support for long options to `make-sqldeveloper-package`
  - Tested against latest release of _SQL Developer_
  - Verified compliancy with _Standards-Version:_ **3.8.1**
  - Bumped version to reflect functionality
- **downloads:**
  - _(unpublished)_

<u>Version <strong>0.1.6</strong></u>
- **changelog:**
  - Modified `make-sqldeveloper-package` to generate a cleaner package, fixing the following lintian info warning:
    - `desktop-entry-contains-encoding-key`
  - Fixed lintian pedantic:
    - `copyright-refers-to-symlink-license`
- **downloads:**
  - _(unpublished)_

<u>Version <strong>0.1.5</strong></u>
- **changelog:**
  - Modified `make-sqldeveloper-package` to generate a clean package, fixing the following lintian warning:
    - `copyright-refers-to-versionless-license-file`
  - Fixed lintian warning:
    - `debhelper-but-no-misc-depends`
  - Corrected an unescaped '`$`' in _Oracle license_ text 
  - Silenced the build process of `make-sqldeveloper-package`
- **downloads:**
  - _(unpublished)_

<u>Version <strong>0.1.4</strong></u>
- **changelog:**
  - Modified `make-sqldeveloper-package` to generate a clean package, fixing the following lintian warnings and errors:
    - `binary-without-manpage`
    - `extra-license-file`
    - `package-contains-empty-directory`
    - `menu-icon-not-in-xpm-format`
    - `debian-revision-should-not-be-zero`
    - `virtual-package-depends-without-real-package-depends`
    - `new-package-should-close-itp-bug` (Closes: [**#515233**](http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=515233))
  - Modified the `sqldeveloper` wrapper script to pass command line parameters to the application
  - Added `-help` and `-version` switches to the `sqldeveloper` wrapper script
- **downloads:**
  - _(unpublished)_

<u>Version <strong>0.1.3</strong></u>
- **changelog:**
  - Fixed a bug introduced with the replacement of `dh_*` scripts by `dh` calls where the wrapper script stopped being renamed
- **downloads:**
  - _(unpublished)_

<u>Version <strong>0.1.2</strong></u>
- **changelog:**
  - Added the _Debian Developer's Reference_ recommendation to auto close the _ITP_ filled against _WNPP_ (Closes: [**#514124**](http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=514124))
- **downloads:**
  - _(unpublished)_

<u>Version <strong>0.1.1</strong></u>
- **changelog:**
  - Modified the install path from `/opt` to `/usr/share`
- **downloads:**
  - _(unpublished)_

<u>Version <strong>0.1.0</strong></u>
- **changelog:**
  - Tested against every release of _SQL Developer_ published to date
  - Bumped version to reflect functionality
- **downloads:**
  - _(unpublished)_

<u>Version <strong>0.0.5</strong></u>
- **changelog:**
  - Modified `make-sqldeveloper-package` to support version **_1.0.0_** of _SQL Developer_
  - Changed documentation to include instructions for earlier _SQL Developer_ releases
- **downloads:**
  - _(unpublished)_

<u>Version <strong>0.0.4</strong></u>
- **changelog:**
  - Fixed the `make-sqldeveloper-package` script to remove unused targets from the `.PHONY` line in the temporary `debian/rules` file.
- **downloads:**
  - _(unpublished)_

<u>Version <strong>0.0.3</strong></u>
- **changelog:**
  - Filled _ITP_ against _WNPP_ ([**#514124**](http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=514124))
  - Moved `make-sqldeveloper-package.1` and `README` to the top level directory
  - Fixed lintian warnings:
    - `dh-clean-k-is-deprecated`
    - `copyright-with-old-dh-make-debian-copyright`
  - Replaced `dh_*` scripts with `dh` calls
  - Modified `make-sqldeveloper-package` to apply the above packaging changes when generating the _sqldeveloper_ package
- **downloads:**
  - _(unpublished)_

<u>Version <strong>0.0.2</strong></u>
- **changelog:**
  - Replaced `xterm` dependency to `x-terminal-emulator` on the `sqldeveloper` wrapper script.
- **downloads:**
  - _(unpublished)_

<u>Version <strong>0.0.1</strong></u>
- **changelog:**
  - Initial Release.
- **downloads:**
  - _(unpublished)_
