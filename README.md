## sqldeveloper-package for Debian and derivatives

**`sqldeveloper-package`** is a small script that will build a [_Debian_](http://www.debian.org) [_package_](http://www.wikipedia.org/wiki/Deb_%28file_format%29) from [_Oracle_](http://www.oracle.com)_'s_ [_SQL Developer_](http://www.oracle.com/technetwork/developer-tools/sql-developer/).

This utility makes it possible to build a _Debian_ package of _Oracle SQL Developer_. The _Oracle SQL Developer_ program is governed by the copyright holder (_Oracle USA, Inc._), so you may be limited as to what you can do with the resulting package (i.e. no redistribution, etc). This utility will simply help you create the _Debian_ package, it is your responsibility to use the resulting package acordingly with the [_OTN license_](http://www.oracle.com/technetwork/licenses/sqldev-license-152021.html), a copy of which is included in the created package, that you must agree on when downloading the source.

This utility will require you to download the **architecture independent** archive from [_\<http://www.oracle.com/technetwork/developer-tools/sql-developer\>_](http://www.oracle.com/technetwork/developer-tools/sql-developer), identified as "**_Oracle SQL Developer for other platforms_**", "**_Oracle SQL Developer for Multiple Platforms_**" or "**_Oracle SQL Developer for Linux and Unix_**" (depending on which version you are building), to create the _Debian_ package from.

<hr width="40%">

<u>The <em>Debian Package</em> <strong><em>sqldeveloper-package</em></strong></u>

In order to run _Oracle SQL Developer_ you'll need a full working [_JDK_](http://www.wikipedia.org/wiki/JDK). The versions that are compatible with _SQL Developer_ are any [_JDK 1.5.0_](http://www.oracle.com/technetwork/java/javasebusiness/downloads/java-archive-downloads-javase5-419410.html)_\_06_ or above or [_JDK 1.6.0_](http://www.oracle.com/technetwork/java/javasebusiness/downloads/java-archive-downloads-javase6-419409.html)_\_03_ or above for _SQL Developer_ versions up to [_1.5.5_](http://www.oracle.com/technetwork/testcontent/index-archive155-099981.html). _SQL Developer_ versions from [_2.1_](http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/index-archive21-092243.html) to [_3.1_](http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/sqldev-31-download-1734499.html) are compatible with [_JDK 1.6.0_](http://www.oracle.com/technetwork/java/javasebusiness/downloads/java-archive-downloads-javase6-419409.html)_\_11_ or above and _SQL Developer_ version [_3.2_](http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/sqldev-downloads-v322-2080107.html) is compatible with [_JDK 1.6.0_](http://www.oracle.com/technetwork/java/javasebusiness/downloads/java-archive-downloads-javase6-419409.html)_\_04_ or above. _SQL Developer_ version [_4.0_](http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/sqldev-downloads-v4-2137727.html) is compatible with [_JDK 1.7_](http://www.oracle.com/technetwork/java/javase/downloads/java-archive-downloads-javase7-521261.html) (_JDK7.0_) series or newer and _SQL Developer_ versions from [_4.1_](http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/sqldev-downloads-41-2592723.html) to [_17.3_](http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/index.html) are compatible with [_JDK 1.8_](http://www.oracle.com/technetwork/java/javase/downloads/java-archive-javase8-2177648.html) (_JDK8.0_) series or newer.

<u><strong>Note</strong> that <em>Oracle SQL Developer</em> prior to version <a href="http://www.oracle.com/technetwork/developer-tools/sql-developer/downloads/sqldev-downloads-v4-2137727.html"><em>4.0</em></a> is <strong>not</strong> compatible with <a href="http://www.oracle.com/technetwork/java/javase/downloads/java-archive-downloads-javase7-521261.html"><em>JDK 1.7</em></a> (<em>JDK7.0</em>) or newer.

There are several ways to obtain a **compatible** _JDK_:
- install [_`default-jdk`_](http://packages.debian.org/search?searchon=names&exact=1&suite=all&section=all&keywords=default-jdk) (java), making sure it depends on the required _JDK_ version
- install one of the required [_`openjdk-6-jdk`_](http://packages.debian.org/search?searchon=names&exact=1&suite=all&section=all&keywords=openjdk-6-jdk), [_`openjdk-7-jdk`_](http://packages.debian.org/search?searchon=names&exact=1&suite=all&section=all&keywords=openjdk-7-jdk), [_`openjdk-8-jdk`_](http://packages.debian.org/search?searchon=names&exact=1&suite=all&section=all&keywords=openjdk-8-jdk) or [_`openjdk-9-jdk`_](http://packages.debian.org/search?searchon=names&exact=1&suite=all&section=all&keywords=openjdk-9-jdk) (java)
- install the meta-package _`java-sdk`_, making sure that it installs the required _JDK_ version as dependency
- install one of the meta-packages _`java6-sdk`_, _`java7-sdk`_, _`java8-sdk`_, or _`java9-sdk`_, making sure that it installs the required _JDK_ version as dependency
- download and run the installer for the version you wish to install from _Oracle_ [_&lt;http://www.oracle.com/technetwork/java/javase/downloads/&gt;_](http://www.oracle.com/technetwork/java/javase/downloads/)
- install [_`java-package`_](http://packages.debian.org/search?searchon=names&exact=1&suite=all&section=all&keywords=java-package) (contrib/misc) and generate a _Debian_ package from the above installer

After installing a **compatible** _JDK_ simply launch _SQL Developer_ through the [_graphical interface_](http://www.wikipedia.org/wiki/Desktop_Linux) or by invoking `/usr/bin/sqldeveloper` and supply the path where the _JDK_ was installed when prompted.

<hr width="40%">

### **Version History**

##### [Version 0.4.4](https://github.com/lazarusllong/sqldeveloper-package/releases/tag/0.4.4):
- **changelog:**
  - Removed `debian/watch` script, it doesn't belong in a _native_ package
- **downloads:**
  - [**`sqldeveloper-package_0.4.4_all.deb`**](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.4.4/sqldeveloper-package_0.4.4_all.deb) (_binary package_)
  - [`sqldeveloper-package_0.4.4.dsc`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.4.4/sqldeveloper-package_0.4.4.dsc) (_source description file_)
  - [`sqldeveloper-package_0.4.4.tar.xz`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.4.4/sqldeveloper-package_0.4.4.tar.xz) (_source code archive_)
  - [`v0.4.2_v0.4.4.debdiff`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.4.4/v0.4.2_v0.4.4.debdiff) (_Debian diff from previous version_)

##### [Version 0.4.3](https://github.com/lazarusllong/sqldeveloper-package/releases/tag/0.4.3):
- **changelog:**
  - Changed author/maintainer email address
  - Generated new _GPG_ key
  - Added `debian/watch` script
- **downloads:**
  - _(unpublished)_

##### [Version 0.4.2](https://github.com/lazarusllong/sqldeveloper-package/releases/tag/0.4.2):
- **changelog:**
  - Fixed _`lintian`_ warning `no-dep5-copyright`
  - Clarified the _JDK_ requirements for **all** _SQL Developer_ version families
- **downloads:**
  - [**`sqldeveloper-package_0.4.2_all.deb`**](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.4.2/sqldeveloper-package_0.4.2_all.deb) (_binary package_)
  - [`sqldeveloper-package_0.4.2.dsc`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.4.2/sqldeveloper-package_0.4.2.dsc) (_source description file_)
  - [`sqldeveloper-package_0.4.2.tar.xz`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.4.2/sqldeveloper-package_0.4.2.tar.xz) (_source code archive_)
  - [`v0.4.1_v0.4.2.debdiff`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.4.2/v0.4.1_v0.4.2.debdiff) (_Debian diff from previous version_)

##### [Version 0.4.1](https://github.com/lazarusllong/sqldeveloper-package/releases/tag/0.4.1):
- **changelog:**
  - Fixed a flaw in the added logic to remove a stale _JVM_ path from configuration, the way the path is stored has changed from _v4.x_ onward (Closes: [**#693798**](https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=693798))
    (Reported by [_Steven Post_](mailto:steven.post@archimiddle.com))
  - Several small fixes and improvements:
    - Fixed the _JDK_ requirements for _SQL Developer_ _v4.0_
    - Added _image thumbnails databases_ to the list of cruft to remove
  - Fixed _`lintian`_ warning `windows-thumbnail-database-in-package`
  - (Re-)Tested against _v3.x_ release family of _SQL Developer_
- **downloads:**
  - [**`sqldeveloper-package_0.4.1_all.deb`**](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.4.1/sqldeveloper-package_0.4.1_all.deb) (_binary package_)
  - [`sqldeveloper-package_0.4.1.dsc`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.4.1/sqldeveloper-package_0.4.1.dsc) (_source description file_)
  - [`sqldeveloper-package_0.4.1.tar.xz`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.4.1/sqldeveloper-package_0.4.1.tar.xz) (_source code archive_)
  - [`v0.3.0_v0.4.1.debdiff`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.4.1/v0.3.0_v0.4.1.debdiff) (_Debian diff from previous version_)

##### [Version 0.4.0](https://github.com/lazarusllong/sqldeveloper-package/releases/tag/0.4.0):
- **changelog:**
  - Addressed all correctable issues and bugs:
    - Separated target from options and disabled check for original file in package build (Closes: [**#868673**](https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=868673))
      (Reported and patch by [_Phil Morrell_](mailto:debian@emorrp1.name))
    - Added logic to wrapper script to remove a stale _JVM_ path from configuration
      (Reported by [_Steven Post_](mailto:steven.post@archimiddle.com))
  - Fixed _`lintian`_ warnings:
    - `ancient-standards-version`
    - `package-uses-deprecated-debhelper-compat-version`
    - `spelling-error-in-description`
  - Modified `make-sqldeveloper-package` to fix _`lintian`_ warnings and errors:
    - `command-in-menu-file-and-desktop-file`
    - `desktop-mime-but-no-exec-code`
    - `extra-license-file`
    - `new-package-should-close-itp-bug`
    - `priority-extra-is-replaced-by-priority-optional`
  - Several small fixes and improvements:
    - Simplified _`debian/rules`_ since `dh_strip_nondeterminism` was heavilly impacting build time by `make-sqldeveloper-package`
    - Added _64-bit foreign DLLs_ to the list of cruft to remove
    - Moved demo files to documentation structure
    - Introduced _`lintian`_ overrides for warnings out of our control:
      - `classpath-contains-relative-path`
      - `codeless-jar`
  - [**New _homepage_**](https://lazarusllong.github.io/sqldeveloper-package/) for the package
  - Updated documentation regarding **compatible** _JDKs_
  - Tested against _v4.x_ and _v17.x_ release families of _SQL Developer_
  - Verified compliancy with Standards-Version: **4.1.1**
  - Bumped version to reflect functionality
- **downloads:**
  - _(unpublished)_

##### [Version 0.3.0](https://github.com/lazarusllong/sqldeveloper-package/releases/tag/0.3.0):
- **changelog:**
  - Addressed all reported issues and bugs:
    - Included `debhelper` on the build dependency list (LP: [**#588458**](https://launchpad.net/bugs/588458))
      (Reported by [_Seth Rosenblum_](https://launchpad.net/~ricklerre))
    - Replaced `dh` options with overrides (LP: [**#998258**](https://launchpad.net/bugs/998258))
      (Reported by [_Christian Loos_](https://launchpad.net/~cloos))
  - Several small fixes and improvements:
    - Fixed an unknown parameter passed to trap when in debug mode
    - Strengthened trap exit handling
    - (Re-)Corrected an unescaped '`$`' in [_OTN license_](http://www.oracle.com/technetwork/licenses/sqldev-license-152021.html) text introduced in the previous version
  - [**New _homepage_**](http://lazarus-corner-of-the-world.blogspot.com/2012/11/sqldeveloper-package.html) for the package
  - Updated documentation regarding compatible _JDKs_
  - Solved _Debian_ QA warnings:
    - Converted source format to 3.0 (native)
    - Added [_Homepage_](http://lazarus-corner-of-the-world.blogspot.com/2012/11/sqldeveloper-package.html) to debian/control
  - Changed the source compression format to xz
  - Verified compliancy with Standards-Version: **3.9.3**
  - Bumped version to reflect functionality
- **downloads:**
  - [**`sqldeveloper-package_0.3.0_all.deb`**](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.3.0/sqldeveloper-package_0.3.0_all.deb) (_binary package_)
  - [`sqldeveloper-package_0.3.0.dsc`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.3.0/sqldeveloper-package_0.3.0.dsc) (_source description file_)
  - [`sqldeveloper-package_0.3.0.tar.xz`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.3.0/sqldeveloper-package_0.3.0.tar.xz) (_source code archive_)
  - [`v0.2.4_v0.3.0.debdiff`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.3.0/v0.2.4_v0.3.0.debdiff) (_Debian diff from previous version_)

##### [Version 0.2.4](https://github.com/lazarusllong/sqldeveloper-package/releases/tag/0.2.4):
- **changelog:**
  - Addressed bugs for inclusion in _Wheezy_'s freeze:
    - Replaced `dos2unix` with `tofrodos` (LP: [**#560803**](https://launchpad.net/bugs/560803),[**#626272**](https://launchpad.net/bugs/626272)) (Closes: [**#568982**](http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=568982))
      (Reported by [_Seth Rosenblum_](https://launchpad.net/~ricklerre))
    - Split `grep` for shell script (LP: [**#985810**](https://launchpad.net/bugs/985810),[**#998610**](https://launchpad.net/bugs/998610)) (Closes: [**#692534**](http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=692534))
      (Reported by [_Bruno Medeiros_](https://launchpad.net/~brunojcm) and patch by [_Brad Powell_](https://launchpad.net/~bradford-powell))
    - Download links updated (Closes: [**#618650**](http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=618650))
      (Reported by [_Sergio Fernandez_](http://bugs.debian.org/cgi-bin/pkgreport.cgi?submitter=sergio%40wikier.org))
  - Fixed _JDK_ dependencies for pre and post _SQL Developer v2_
  - Updated documentation regarding above changes
  - Updated [_OTN license_](http://www.oracle.com/technetwork/licenses/sqldev-license-152021.html) information to current version
  - Tested against v2.x and v3.x release families of _SQL Developer_
  - Bumped version to reflect functionality
- **downloads:**
  - [**`sqldeveloper-package_0.2.4_all.deb`**](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.2.4/sqldeveloper-package_0.2.4_all.deb) (_binary package_)
  - [`sqldeveloper-package_0.2.4.dsc`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.2.4/sqldeveloper-package_0.2.4.dsc) (_source description file_)
  - [`sqldeveloper-package_0.2.4.tar.gz`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.2.4/sqldeveloper-package_0.2.4.tar.gz) (_source code archive_)
  - [`v0.2.3_v0.2.4.debdiff`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.2.4/v0.2.3_v0.2.4.debdiff) (_Debian diff from previous version_)

##### [Version 0.2.3+nmu1](https://github.com/lazarusllong/sqldeveloper-package/releases/tag/0.2.3+nmu1):
- **changelog:**
  - Non-maintainer upload.
  - Use `fromdos` in place of gone `dos2unix` for CRLF conversion management. Remove no longer needed alternative dep on `sysutils`, which is gone too. Patch from Michael Musenbrock. (Closes: [**#568982**](http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=568982))
- **downloads:**
  - [**`sqldeveloper-package_0.2.3+nmu1_all.deb`**](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.2.3+nmu1/sqldeveloper-package_0.2.3+nmu1_all.deb) (_binary package_)
  - [`sqldeveloper-package_0.2.3+nmu1.dsc`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.2.3+nmu1/sqldeveloper-package_0.2.3+nmu1.dsc) (_source description file_)
  - [`sqldeveloper-package_0.2.3+nmu1.tar.gz`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.2.3+nmu1/sqldeveloper-package_0.2.3+nmu1.tar.gz) (_source code archive_)

##### [Version 0.2.3](https://github.com/lazarusllong/sqldeveloper-package/releases/tag/0.2.3):
- **changelog:**
  - Fixed the command line options `-m`\|`--maintainer` option which was not getting the current login
- **downloads:**
  - [**`sqldeveloper-package_0.2.3_all.deb`**](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.2.3/sqldeveloper-package_0.2.3_all.deb) (_binary package_)
  - [`sqldeveloper-package_0.2.3.dsc`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.2.3/sqldeveloper-package_0.2.3.dsc) (_source description file_)
  - [`sqldeveloper-package_0.2.3.tar.gz`](https://github.com/lazarusllong/sqldeveloper-package/releases/download/0.2.3/sqldeveloper-package_0.2.3.tar.gz) (_source code archive_)

##### _Version 0.2.2_:
- **changelog:**
  - Modified `make-sqldeveloper-package` to not default to the author name and email for the _Maintainer:_ field of the _Debian_ package as follows: if command line options `-m`\|`--maintainer` and/or `-e`\|`--email` are set then use these, else if `DEBFULLNAME` and/or `DEBEMAIL` environment variables are set then use these, else default the _Maintainer_ name to an empty string and/or generate the _Maintainer_ email from the current login and hostname
- **downloads:**
  - _(unpublished)_

##### _Version 0.2.1_:
- **changelog:**
  - Rearranged `make-sqldeveloper-package` help output to fit without wrapping in 80 columns
  - Rewrote the `sqldeveloper` wrapper script fixing all issues reported by `checkbashisms`
  - Modified the versioning of the resulting _Debian_ package to include the version of `make-sqldeveloper-package` used to build it
  - Changed the _Priority:_ from `optional` to `extra` for the resulting _Debian_ package
  - Modified the `make-sqldeveloper-package` to honor the `DEBFULLNAME` and `DEBEMAIL` environment variables for the _Maintainer:_ field of the _Debian_ package as follows: if command line options `-m`\|`--maintainer` and/or `-e`\|`--email` are set then use these, else if `DEBFULLNAME` and/or `DEBEMAIL` environment variables are set then use these, else default to the author name and email
  - Changed all negative exit and return values to positive integers
- **downloads:**
  - _(unpublished)_

##### _Version 0.2.0_:
- **changelog:**
  - Rewrote the `make-sqldeveloper-package` fixing all issues reported by `checkbashisms` (thanks to [_Nelson A. de Oliveira_](mailto:naoliv@debian.org) who reported this)
  - Added support for long options to `make-sqldeveloper-package`
  - Tested against latest release of _SQL Developer_
  - Verified compliancy with Standards-Version: **3.8.1**
  - Bumped version to reflect functionality
- **downloads:**
  - _(unpublished)_

##### _Version 0.1.6_:
- **changelog:**
  - Modified `make-sqldeveloper-package` to generate a cleaner package, fixing the following _`lintian`_ info warning:
    - `desktop-entry-contains-encoding-key`
  - Fixed _`lintian`_ pedantic:
    - `copyright-refers-to-symlink-license`
- **downloads:**
  - _(unpublished)_

##### _Version 0.1.5_:
- **changelog:**
  - Modified `make-sqldeveloper-package` to generate a clean package, fixing the following _`lintian`_ warning:
    - `copyright-refers-to-versionless-license-file`
  - Fixed _`lintian`_ warning:
    - `debhelper-but-no-misc-depends`
  - Corrected an unescaped '`$`' in _Oracle license_ text 
  - Silenced the build process of `make-sqldeveloper-package`
- **downloads:**
  - _(unpublished)_

##### _Version 0.1.4_:
- **changelog:**
  - Modified `make-sqldeveloper-package` to generate a clean package, fixing the following _`lintian`_ warnings and errors:
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

##### _Version 0.1.3_:
- **changelog:**
  - Fixed a bug introduced with the replacement of `dh_*` scripts by `dh` calls where the wrapper script stopped being renamed
- **downloads:**
  - _(unpublished)_

##### _Version 0.1.2_:
- **changelog:**
  - Added the _Debian Developer's Reference_ recommendation to auto close the _ITP_ filled against _WNPP_ (Closes: [**#514124**](http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=514124))
- **downloads:**
  - _(unpublished)_

##### _Version 0.1.1_:
- **changelog:**
  - Modified the install path from `/opt` to `/usr/share`
- **downloads:**
  - _(unpublished)_

##### _Version 0.1.0_:
- **changelog:**
  - Tested against every release of _SQL Developer_ published to date
  - Bumped version to reflect functionality
- **downloads:**
  - _(unpublished)_

##### _Version 0.0.5_:
- **changelog:**
  - Modified `make-sqldeveloper-package` to support version **_1.0.0_** of _SQL Developer_
  - Changed documentation to include instructions for earlier _SQL Developer_ releases
- **downloads:**
  - _(unpublished)_

##### _Version 0.0.4_:
- **changelog:**
  - Fixed the `make-sqldeveloper-package` script to remove unused targets from the `.PHONY` line in the temporary `debian/rules` file.
- **downloads:**
  - _(unpublished)_

##### _Version 0.0.3_:
- **changelog:**
  - Filled _ITP_ against _WNPP_ ([**#514124**](http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=514124))
  - Moved `make-sqldeveloper-package.1` and `README` to the top level directory
  - Fixed _`lintian`_ warnings:
    - `dh-clean-k-is-deprecated`
    - `copyright-with-old-dh-make-debian-copyright`
  - Replaced `dh_*` scripts with `dh` calls
  - Modified `make-sqldeveloper-package` to apply the above packaging changes when generating the _sqldeveloper_ package
- **downloads:**
  - _(unpublished)_

##### _Version 0.0.2_:
- **changelog:**
  - Replaced `xterm` dependency to `x-terminal-emulator` on the `sqldeveloper` wrapper script.
- **downloads:**
  - _(unpublished)_

##### _Version 0.0.1_:
- **changelog:**
  - Initial Release.
- **downloads:**
  - _(unpublished)_
