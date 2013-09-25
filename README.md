mangos-zero, a World of Warcraft server for vanilla WoW  [![Build status](https://travis-ci.org/mangoszero/server.png)][16] [![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/mangoszero/server/trend.png)](https://bitdeli.com/free "Bitdeli Badge")
=======================================================
*mangos-zero* is open source, built in [C++][7], fast, runs on multiple platforms,
can store game data in [MySQL][40] and [PostgreSQL][42]. It has optional support
for SOAP, and aims to be 100% compatible with [World of Warcraft][2] in its
vanilla versions, namely [patch 1.12.1][5] and [patch 1.12.2][6].

If you like the first incarnation of WoW, and still fancy [vanilla WoW][4],
you should try *mangos-zero*. We provide an authentication server where you can
manage your users, and a world server which serves game content just like
the original [WoW][2] did back then.

On top of that each update is built by [Travis CI][16] as you can see by the
image next to the chapter's heading! We do love green builds, and working things.
To complement this, we push builds through [Coverity][17] to find and fix any
possible security issues.

World of Warcraft, and all World of Warcraft or Warcraft art, images, and lore are
copyrighted by [Blizzard Entertainment, Inc.][1]

Requirements
------------
*mangos-zero server* supports a wide range of operating systems, and various
compiler platforms. In order to do that, we use various free cross-platform
libraries and use [CMake][19] to provide a cross-platform build system which
adapts to your chosen operating system and compiler.

Operating systems
-----------------
Currently we do support running the server on these operating systems:

* **Windows**, 32bit and 64bit. [Windows][20] 7 is recommended.
* **Linux**, 32bit and 64bit. [Debian 7][21] and [Ubuntu 12.04 LTS][22] are
  recommended.
* **BSD**, 32bit and 64bit. [FreeBSD][23], [NetBSD][24], [OpenBSD][25] and
  [DragonFly][26] are recommended.

Of course, newer versions should work, too. In case of Windows, matching
server version will work, too.

Compilers
---------
Building the server is currently possible with these compilers:

* **Microsoft Visual Studio (Express[^1])**, 32bit and 64bit. Both the
  [Visual Studio Express][30] and the professional [Visual Studio][31]
  editions are supported.
* **Microsoft Windows SDK**, 32bit and 64bit. The [Windows 7 SDK][32] is
  recommeded, as older versions lack compiler features required to build
  the server.
* **Clang**, 32bit and 64bit. The [Clang compiler][33] can be used to build
  the server on any supported operating system.[^2]

Dependencies
------------
*mangos-zero server* stands on the shoulds of a few well-known Open Source
libraries, and a few awesome, but less common libraries to prevent us from
inventing the wheel again.

* **MySQL** / **PostgreSQL**: to store content, and user data, we rely on
  [MySQL][40]/[MariaDB][41] and [PostgreSQL][42] to handle data.
* **ACE**: the [ADAPTIVE Communication Environment][43] aka. *ACE* provides us
  with a solid cross-platform framework for abstracting operating system
  specific details.
* **Recast**: in order to create navigation data from the client's map files,
  we use [Recast][44] to do the dirty work. It provides functions for
  rendering, pathing, etc.
* **G3D**: the [G3D][45] engine provides the basic framework for handling 3D
  data, and is used to handle basic map data.
* **libmpq**: [libmpq][46] provides an abstraction layer for reading from the
  client's data files.

Optional dependencies
---------------------
* **Intel TBB**: the [Threading Building Blocks][47] provide a convenient
  cross-platform abstraction for parallel programming.

Discuss
-------
If you need help with building and installing *mangos-zero* there is thousands
of users out there already running *mangos-zero* and many you can find online

* project website: [getmangos.com][10]
* discussion forums: [community.getmangos.co.uk][11]

License
-------
This program is free software; you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation; either version 2 of the License, or (at your option) any later
version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with
this program; if not, write to the Free Software Foundation, Inc., 51 Franklin
Street, Fifth Floor, Boston, MA 02110-1301 USA.

The full license is included in the file `License.md`.

In addition, as a special exception, permission is granted to link the code of
*mangos-zero* with the OpenSSL project's [OpenSSL library][48] (or with modified
versions of it that use the same license as the OpenSSL library), and distribute
the linked executables. You must obey the GNU General Public License in all
respects for all of the code used other than [OpenSSL][48].


[^1]: Visual Studio Express versions prior to the 2012 release can only
      build 32 bit applications, unless you install the Windows SDK.
[^2]: Clang support for Windows is experimental. Failure to compile the
      server may also relate to the experimental state of the port.

[1]: http://blizzard.com/ "Blizzard Entertainment Inc. · we love you!"
[2]: http://blizzard.com/games/wow/ "World of Warcraft · Classic / Vanilla"
[3]: http://wowpedia.org/Beta#World_of_Warcraft "World of Warcraft - Classic Beta"
[4]: http://www.wowpedia.org/Patch_1.12.0 "Vanilla WoW · Patch 1.12.0 release notes"
[5]: http://www.wowpedia.org/Patch_1.12.1 "Vanilla WoW · Patch 1.12.1 release notes"
[6]: http://www.wowpedia.org/Patch_1.12.2 "Vanilla WoW · Patch 1.12.2 release notes"
[7]: http://www.cppreference.com/ "C / C++ reference"

[10]: http://getmangos.com/ "mangos · project site"
[11]: http://community.getmangos.co.uk/ "mangos · discussion forums"
[12]: http://github.com/mangoszero "mangos-zero · github organization"
[13]: http://github.com/mangoszero/server "mangos zero · server repository"
[14]: http://github.com/mangoszero/scripts "mangos zero · script extensions repository"
[15]: http://github.com/mangoszero/database "mangos zero · content database repository"
[16]: https://travis-ci.org/mangoszero/server "Travis CI · mangos-zero build status"
[17]: https://scan.coverity.com/ "Coverity Scan · Static Code Analysis"

[19]: http://www.cmake.org/ "CMake · Cross Platform Make"
[20]: http://windows.microsoft.com/ "Microsoft Windows · that OS, yes."
[21]: http://www.debian.org/ "Debian · The Universal Operating System"
[22]: http://www.ubuntu.com/ "Ubuntu · The world's most popular free OS"
[23]: http://www.freebsd.org/ "FreeBSD · The Power To Serve"
[24]: http://www.netbsd.org/ "NetBSD · The NetBSD Project"
[25]: http://www.openbsd.org/ "OpenBSD · Free, functional and secure"
[26]: http://www.dragonflybsd.org/ "DragonFlyBSD"

[30]: http://www.microsoft.com/visualstudio/eng/ "Visual Studio 2012"
[31]: http://www.microsoft.com/visualstudio/eng/products/visual-studio-express-products "Visual Studio Express 2012 for Windows Desktop"
[32]: http://www.microsoft.com/en-us/download/details.aspx?id=8279 "Windows SDK for Windows 7 and .NET Framework 4"
[33]: http://clang.llvm.org/ "clang: a C language family frontend for LLVM"

[40]: http://www.mysql.com/ "MySQL · The world's most popular open source database"
[41]: http://www.mariadb.org/ "MariaDB · An enhanced, drop-in replacement for MySQL"
[42]: http://www.postgresql.org/ "PostgreSQL · The world's most advanced open source database"
[43]: http://www.cs.wustl.edu/~schmidt/ACE.html "ACE · The ADAPTIVE Communication Environment"
[44]: http://github.com/memononen/recastnavigation "Recast · Navigation-mesh Toolset for Games"
[45]: http://sourceforge.net/projects/g3d/ "G3D Innovation Engine"
[46]: http://github.com/ge0rg/libmpq "libmpq"
[47]: http://www.threadingbuildingblocks.org/ "Intel Threading Building Blocks · TBB"
[48]: http://www.openssl.org/ "OpenSSL"
